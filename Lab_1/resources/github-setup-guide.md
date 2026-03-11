# GitHub Repository Setup Guide

**Course:** CS-PD-2026  
**Used in:** Lab 1 (and ongoing throughout the semester)  

This repository is your team's evidence base for 15 weeks. Set it up correctly in the first lab and you will not have to fix structural issues later when the stakes are higher.

---

## Step 1: Create the Repository

**Who does this:** Tech Lead

1. Go to the course GitHub organisation: `https://github.com/ZA-KIU-Classroom`
2. Click **New Repository**
3. Name it exactly: `product-capstone-2026`
   - Note: if the organisation auto-prefixes team names, use whatever the organisation specifies -- confirm with your instructor
4. Set visibility to **Public** (required for instructor grading)
5. Check **Add a README file** -- this creates the main branch automatically
6. For **.gitignore**, select the template closest to your primary language. If you do not know yet, select **Node** as a reasonable default.
7. Leave the license blank for now.
8. Click **Create repository**

---

## Step 2: Add All Team Members as Collaborators

**Who does this:** Tech Lead

1. In the repository, go to **Settings > Collaborators**
2. Click **Add people** and search for each team member's GitHub username
3. Set their role to **Write**
4. Each team member will receive an email invitation -- they must accept it before they can push

**Do not leave lab until every team member has accepted their invitation and confirmed they can push.** This is a lab day blocker that becomes a problem on Sunday night if not resolved now.

---

## Step 3: Create the Folder Structure

GitHub does not allow empty folders. Create each folder by adding a placeholder file inside it.

**Option A (in the GitHub web interface, faster in lab):**

1. In the repository, click **Add file > Create new file**
2. In the filename field, type: `00-foundation/.gitkeep`
3. Leave the content blank
4. Click **Commit new file** with the message: `[LAB-1] Create 00-foundation folder`
5. Repeat for `01-discovery/.gitkeep` and `milestones/.gitkeep`

**Option B (via command line, better practice):**

```bash
# Clone the repository
git clone https://github.com/ZA-KIU-Classroom/product-capstone-2026.git
cd product-capstone-2026

# Create folders with placeholder files
mkdir -p 00-foundation 01-discovery milestones
touch 00-foundation/.gitkeep
touch 01-discovery/.gitkeep
touch milestones/.gitkeep

# Commit and push
git add .
git commit -m "[LAB-1] Create initial folder structure"
git push origin main
```

---

## Step 4: Confirm Everyone Can Clone and Push

**Who does this:** Every team member individually

```bash
# Clone the repository (if you have not already)
git clone https://github.com/ZA-KIU-Classroom/product-capstone-2026.git
cd product-capstone-2026

# Make a small test commit to confirm push access
echo "# Test commit by [your name]" >> README.md
git add README.md
git commit -m "[LAB-1] Test push from [your name]"
git push origin main
```

If the push succeeds, you have access. If it fails with a permissions error, check that you accepted the collaborator invitation in your email.

---

## Step 5: Configure Your .gitignore

If you did not select a `.gitignore` template at creation, add one now. At minimum, the file should exclude:

```
# macOS
.DS_Store
.AppleDouble
.LSOverride

# Windows
Thumbs.db
Desktop.ini

# JetBrains IDEs
.idea/
*.iml

# VS Code
.vscode/

# Node (if applicable)
node_modules/
npm-debug.log*

# Python (if applicable)
__pycache__/
*.py[cod]
.env
venv/

# Compiled output
dist/
build/
*.o
*.a
*.so
```

You will update this file as you learn more about your tech stack.

---

## Step 6: Create and Update the README

The repository root `README.md` should be updated by end of lab to include at minimum:

```markdown
# [Your Team Name] -- Product Capstone 2026

**Course:** CS-PD-2026 Product Development for Software Engineers  
**Semester:** Spring 2026  
**Institution:** Kutaisi International University  

## Team

| Name | Role | GitHub |
|------|------|--------|
| [Name] | Program Lead | @[username] |
| [Name] | Discovery Lead | @[username] |
| [Name] | Tech Lead | @[username] |

## Project

We are currently in the problem discovery phase (Week 2). Problem selection happens in Lab 2.

## Repository Structure

- `00-foundation/` -- Team contract, problem statements, ICP
- `01-discovery/` -- Interview scripts, logs, and synthesis
- `milestones/` -- Weekly milestone tracking documents

## Status

Week 2 -- Team formation complete. Problem brainstorming in progress.
```

---

## Making Good Commits

Every commit you make in this repository is visible to the instructor and becomes part of your evidence trail. Treat commit messages as professional documentation.

**Format:**
```
[LAB-X] Brief description of what this commit contains
```

**Examples:**
```
[LAB-1] Add team-contract.md with roles and conflict protocol
[LAB-1] Add all-problem-statements.md with brainstorm output from all 3 members
[LAB-2] Add team-icp.md with finalised ICP after Four Filters session
```

**What makes a bad commit message:**
- `update`
- `fix stuff`
- `added file`
- `wip`

A good commit message tells the grader what they will find inside the commit without having to open the diff. This is standard professional practice.

---

## Troubleshooting

**"I cannot push -- permission denied"**  
Check that you accepted the collaborator invitation from your email. If the invitation has expired (GitHub invitations expire after 7 days), ask the Tech Lead to resend it.

**"There is a merge conflict"**  
This happens when two people edit the same file simultaneously. To resolve:
```bash
git pull origin main
# Git will highlight the conflict in the file with <<<< and >>>> markers
# Open the file, decide which version to keep, delete the markers
git add [filename]
git commit -m "Resolve merge conflict in [filename]"
git push origin main
```

If this is confusing, call the instructor over. Resolving your first merge conflict in a low-stakes moment is much better than encountering it for the first time the night before Checkpoint 1.

**"My changes are not showing up on GitHub"**  
You have committed but not pushed, or you pushed to the wrong branch.
```bash
git status          # Shows uncommitted changes
git log --oneline   # Shows recent commits
git push origin main
```

---

## Submission Tag

For all lab submissions you will create a Git tag:

```bash
git tag lab-1-submission
git push origin main --tags
```

A tag is a named marker on a specific commit. It tells the grader: "This is the state of the repository at the time I submitted." If you make corrections after the deadline and push them, the tag still points to the original submission.

---

*CS-PD-2026 | Kutaisi International University | Spring 2026*
