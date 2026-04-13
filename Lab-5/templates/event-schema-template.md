# Event Schema

**Team:** [Your Team Name]  
**Product:** [Your Product Name]  
**Date:** [Date]  
**Version:** 1.0  
**Status:** Blueprint (instrumentation code written in Lab 6)

---

## Naming Convention

All events follow this rule without exception:

```
object_action (snake_case, past tense)
```

Examples of correct names: `user_signup_completed`, `booking_created`, `space_search_started`  
Examples of incorrect names: `UserSignupCompleted`, `create_booking`, `search`, `click_button`

---

## North Star Metric

> [Paste your NSM here from north-star-metric.md]

**Activation event that drives NSM:** `[event_name]`

---

## Universal Properties

Every event automatically includes these properties. Do not repeat them in individual event definitions.

| Property | Type | Description |
|----------|------|-------------|
| `user_id` | string (UUID) | System-generated user identifier. Never an email address. |
| `timestamp` | ISO 8601 datetime | When the event fired. Always include timezone (Z for UTC). |
| `session_id` | string (UUID) | The session in which the event occurred. |
| `platform` | enum: web, ios, android | The platform the event was fired on. |

---

## Event Definitions

### ACQUISITION

---

#### `[event_name]`

**AARRR Stage:** Acquisition  
**Description:** [What the user did that triggered this event]  
**Fires when:** [Exact trigger condition]  
**NSM connection:** [How this event connects to your NSM, or "None -- acquisition only"]

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `[property_name]` | string | Yes | [What this captures] | `"[example value]"` |
| `[property_name]` | enum | Yes | [Allowed values] | `"[example value]"` |
| `[property_name]` | boolean | No | [What this captures] | `true` |

**Example payload:**
```json
{
  "event_name": "[event_name]",
  "user_id": "user_abc123",
  "timestamp": "2026-04-09T14:23:45Z",
  "session_id": "sess_xyz789",
  "platform": "web",
  "[property_name]": "[example value]"
}
```

---

#### `[event_name]`

**AARRR Stage:** Acquisition  
**Description:** [What the user did]  
**Fires when:** [Trigger condition]  
**NSM connection:** [Connection or "None"]

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `[property_name]` | string | Yes | [Description] | `"[example]"` |

---

### ACTIVATION

---

#### `[event_name]` ← THIS IS YOUR ACTIVATION EVENT

**AARRR Stage:** Activation  
**Description:** [The aha moment. The user got value for the first time.]  
**Fires when:** [Exact trigger -- be precise]  
**NSM connection:** This event directly drives the NSM. Each firing of this event increments [describe how].

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `[property_name]` | string | Yes | [Description] | `"[example]"` |
| `[property_name]` | integer | Yes | [Description] | `[example]` |
| `[property_name]` | float | No | [Description] | `[example]` |

**Example payload:**
```json
{
  "event_name": "[event_name]",
  "user_id": "user_abc123",
  "timestamp": "2026-04-09T14:23:45Z",
  "session_id": "sess_xyz789",
  "platform": "web",
  "[property_name]": "[example value]",
  "[property_name]": "[example value]"
}
```

---

### RETENTION

---

#### `[event_name]`

**AARRR Stage:** Retention  
**Description:** [The user returned and did the core action again]  
**Fires when:** [Trigger condition]  
**NSM connection:** [How this contributes to tracking whether the NSM is sustained over time]

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `[property_name]` | string | Yes | [Description] | `"[example]"` |
| `[property_name]` | integer | No | [e.g. How many times they have done this action total] | `[example]` |

---

### REFERRAL

---

#### `[event_name]`

**AARRR Stage:** Referral  
**Description:** [The user shared or invited someone]  
**Fires when:** [Trigger condition]  
**NSM connection:** [Connection or "None -- referral only"]

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `[property_name]` | string | Yes | [Description] | `"[example]"` |
| `[property_name]` | enum | No | [How they shared] | `"[example]"` |

---

### REVENUE (if applicable)

---

#### `[event_name]`

**AARRR Stage:** Revenue  
**Description:** [The user converted to a paid action]  
**Fires when:** [Trigger condition]  
**NSM connection:** [Connection or "Not applicable for MVP -- no paid tier yet"]

| Property | Type | Required | Description | Example |
|----------|------|----------|-------------|---------|
| `[property_name]` | float | Yes | [e.g. Amount paid in USD] | `[example]` |
| `[property_name]` | string | Yes | [e.g. Plan selected] | `"[example]"` |

---

## Event Summary Table

| Event Name | AARRR Stage | Priority | NSM Driver |
|-----------|-------------|----------|-----------|
| `[event_name]` | Acquisition | Must | No |
| `[event_name]` | Acquisition | Must | No |
| `[event_name]` | Activation | Must | Yes |
| `[event_name]` | Retention | Must | Indirect |
| `[event_name]` | Referral | Should | No |
| `[event_name]` | Revenue | If applicable | No |

**Total events:** [Count]  
**Must-have events:** [Count]  
**Should-have events:** [Count]

---

## Privacy Confirmation

Confirm that no event in this schema captures PII:

- [ ] No email addresses in any event property
- [ ] No user names or display names in any event property
- [ ] No phone numbers in any event property
- [ ] No physical addresses in any event property
- [ ] No payment card details in any event property
- [ ] All user identification uses system-generated UUIDs only

**Schema reviewed by:** [Name] on [Date]

---

## Instrumentation Notes for Lab 6

This is the blueprint only. In Lab 6, you will write the actual code to fire these events in your Google AI Studio app.

For each event, note where in the application flow it fires:

| Event Name | Where in Code | Frontend or Backend |
|-----------|--------------|-------------------|
| `[event_name]` | [e.g. On signup form submission success callback] | Frontend |
| `[event_name]` | [e.g. After database booking record created] | Backend |
| `[event_name]` | [e.g. On page load for authenticated user] | Frontend |

---

## Analytics Tool Selection

Which tool will you use to receive and store your events?

- [ ] Mixpanel (best for funnel analysis)
- [ ] Amplitude (best for retention curves)
- [ ] PostHog (best for self-hosted, privacy-conscious products)
- [ ] Google Analytics 4 (best for web-only MVPs)

**Our choice:** [Tool name]  
**Reason:** [One sentence]  
**Free tier limit:** [e.g. Mixpanel: 20M events per month]

---

## Change Log

| Date | Version | Changes | Author |
|------|---------|---------|--------|
| [Date] | 1.0 | Initial schema blueprint | [Name] |

---

*Event Schema | [Team Name] | CS-PD-2026 | Spring 2026*
