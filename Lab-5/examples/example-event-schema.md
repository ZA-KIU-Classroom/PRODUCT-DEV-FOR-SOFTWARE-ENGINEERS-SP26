# EXAMPLE: Event Schema
## StudySpace Finders | CS-PD-2026 Example Team

*This is a worked example. Do not copy this. Your schema must reflect your own product's user flows.*

---

## Naming Convention

All events: `object_action` (snake_case, past tense)

---

## North Star Metric

> Weekly study sessions booked per active user

**Activation event that drives NSM:** `booking_completed`

---

## Universal Properties

Every event automatically includes:

| Property | Type | Description |
|----------|------|-------------|
| `user_id` | string (UUID) | System-generated. Never an email address. |
| `timestamp` | ISO 8601 datetime | Always UTC (Z suffix). |
| `session_id` | string (UUID) | The app session. Resets on new login. |
| `platform` | enum: web | MVP is web-only. |

---

## Event Definitions

### ACQUISITION

---

#### `user_signup_started`

**AARRR Stage:** Acquisition  
**Description:** User begins the registration process by clicking "Sign Up" or navigating to the signup page.  
**Fires when:** User loads the signup form.  
**NSM connection:** None directly. Measures the top of the acquisition funnel.

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `signup_method` | enum: email, google, github | Yes | How the user chose to sign up | `"google"` |
| `referral_source` | string | No | UTM source if present, else null | `"instagram_bio"` |

**Example payload:**
```json
{
  "event_name": "user_signup_started",
  "user_id": "user_abc123",
  "timestamp": "2026-04-09T14:15:00Z",
  "session_id": "sess_xyz789",
  "platform": "web",
  "signup_method": "google",
  "referral_source": null
}
```

---

#### `user_signup_completed`

**AARRR Stage:** Acquisition  
**Description:** User successfully creates an account and lands on the home screen for the first time.  
**Fires when:** Account creation succeeds and the user is redirected to the authenticated home screen.  
**NSM connection:** None directly. Marks the start of the activation funnel.

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `signup_method` | enum: email, google, github | Yes | How the user signed up | `"google"` |
| `time_to_complete_seconds` | integer | Yes | Seconds from signup_started to signup_completed | `47` |

---

### ACTIVATION

---

#### `booking_completed` ← THIS IS THE ACTIVATION EVENT

**AARRR Stage:** Activation  
**Description:** User successfully completes a study space booking. This is the aha moment. The user now has a confirmed space to study.  
**Fires when:** The booking record is created in the database and the confirmation screen is shown.  
**NSM connection:** Each firing of this event increments the weekly booking count for this user_id. This directly drives the NSM.

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `space_id` | string (UUID) | Yes | The space that was booked | `"space_44f2a"` |
| `space_category` | enum: library, cafe, university_room, coworking | Yes | Type of space | `"library"` |
| `time_slot` | enum: morning, afternoon, evening | Yes | Which time slot was booked | `"afternoon"` |
| `booking_date` | string (YYYY-MM-DD) | Yes | The date of the booking | `"2026-04-10"` |
| `search_to_booking_seconds` | integer | Yes | Time from space_search_started to booking_completed | `183` |
| `is_first_booking` | boolean | Yes | True if this is the user's first ever booking | `true` |

**Example payload:**
```json
{
  "event_name": "booking_completed",
  "user_id": "user_abc123",
  "timestamp": "2026-04-09T14:23:45Z",
  "session_id": "sess_xyz789",
  "platform": "web",
  "space_id": "space_44f2a",
  "space_category": "library",
  "time_slot": "afternoon",
  "booking_date": "2026-04-10",
  "search_to_booking_seconds": 183,
  "is_first_booking": true
}
```

---

#### `space_search_started`

**AARRR Stage:** Activation  
**Description:** User submits the search form to find available spaces.  
**Fires when:** User taps the Search button with a valid location and date selected.  
**NSM connection:** Indirect. This begins the flow that leads to booking_completed. High search-to-booking drop-off indicates a search quality problem.

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `search_location` | string | Yes | The location string entered (not GPS coordinates) | `"Kutaisi City Centre"` |
| `time_slot` | enum: morning, afternoon, evening | Yes | Selected time slot | `"afternoon"` |
| `search_date` | string (YYYY-MM-DD) | Yes | The date searched for | `"2026-04-10"` |

---

### RETENTION

---

#### `user_session_started`

**AARRR Stage:** Retention  
**Description:** An existing user opens the app and begins a new session. Used to measure Day 1, Day 7, and Day 30 retention.  
**Fires when:** An authenticated user loads the home screen.  
**NSM connection:** Indirect. A user who returns but does not book is partially retained. A user who returns and books is fully retained.

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `days_since_signup` | integer | Yes | Days since user_signup_completed | `7` |
| `days_since_last_session` | integer | Yes | Days since previous user_session_started | `3` |
| `total_bookings_lifetime` | integer | Yes | Total booking_completed events for this user | `4` |

---

### REFERRAL

---

#### `invite_sent`

**AARRR Stage:** Referral  
**Description:** User shares the app with a friend via the in-app invite feature.  
**Fires when:** User taps Send on the invite flow and the invite is dispatched.  
**NSM connection:** None directly. Referral loop expands acquisition.

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `invite_method` | enum: link_copy, whatsapp, email | Yes | How the user sent the invite | `"whatsapp"` |

---

## Event Summary Table

| Event Name | AARRR Stage | Priority | NSM Driver |
|-----------|-------------|----------|-----------|
| `user_signup_started` | Acquisition | Must | No |
| `user_signup_completed` | Acquisition | Must | No |
| `space_search_started` | Activation | Must | Indirect |
| `booking_completed` | Activation | Must | **Yes -- primary** |
| `user_session_started` | Retention | Must | Indirect |
| `invite_sent` | Referral | Should | No |

**Total events:** 6  
**Must-have events:** 5  
**Should-have events:** 1

---

## Privacy Confirmation

- [x] No email addresses in any event property
- [x] No user names or display names in any event property
- [x] No phone numbers in any event property
- [x] No physical addresses in any event property
- [x] No payment card details in any event property
- [x] All user identification uses system-generated UUIDs only

**Schema reviewed by:** Dato (Engineering Lead) on 9 April 2026

---

## Instrumentation Notes for Lab 6

| Event Name | Where in Code | Frontend or Backend |
|-----------|--------------|-------------------|
| `user_signup_started` | On signup page mount (useEffect) | Frontend |
| `user_signup_completed` | In POST /api/auth/register success callback | Backend |
| `space_search_started` | On Search form submit handler | Frontend |
| `booking_completed` | In POST /api/bookings success callback, after DB write confirms | Backend |
| `user_session_started` | In authenticated layout component on mount | Frontend |
| `invite_sent` | In POST /api/invites success callback | Backend |

---

## Analytics Tool Selection

**Our choice:** Mixpanel  
**Reason:** Best free-tier funnel analysis and we need to measure the search-to-booking conversion rate clearly.  
**Free tier limit:** 20M events per month (more than sufficient for MVP)

---

*Example Document | StudySpace Finders | CS-PD-2026 | Spring 2026*
