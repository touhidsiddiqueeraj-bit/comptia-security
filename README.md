# CompTIA Security+ SY0-701 — Zero to Hero Study App

A self-contained, single-file study app for the **CompTIA Security+ SY0-701** exam. 60-day structured study plan with practice quizzes, progress tracking, and optional cloud sync via Google Sheets.



Live at: https://touhidsiddiqueeraj-bit.github.io/comptia-security/


## Features

- **60-day study plan** across 6 domains aligned to SY0-701 exam objectives

- **6 study domains**: General Security → Threats & Attacks → Security Operations → IRM & Governance → Review & PBQ → Final Audit

- **Daily checklists** with curated YouTube video links for each topic

- **Practice quizzes** with multiple choice questions and instant feedback

- **XP & leveling system** to keep you motivated

- **Streak tracking** and study heatmap

- **Light/dark mode** toggle

- **Progress sync** via Google Sheets (optional — see backend setup below)

- **Fully offline capable** — works without the backend


## Files

| File | Description |
| - | - |
| `CompTIA-Security.html` | The complete frontend app — open in any browser |
| `GOOGLE\_APPS\_SCRIPT\_Security.gas` | Backend script for user accounts & cloud progress sync |



## Quick Start (No Backend)

1. Download `CompTIA-Security.html`

2. Open it in any modern browser (Chrome, Firefox, Edge)

3. Progress is saved to `localStorage` automatically — no account needed


## Full Setup (With Cloud Sync)

To enable multi-device progress sync and user accounts, deploy the Google Apps Script backend:

### Step 1 — Create the Google Sheet

1. Go to [sheets.google.com](https://sheets.google.com/) and create a new blank spreadsheet

2. Rename `Sheet1` to **Users**

3. Add a second sheet named **Progress**

### Step 2 — Deploy the Apps Script

1. In your spreadsheet, go to **Extensions → Apps Script**

2. Delete any existing code and paste the entire contents of `GOOGLE\_APPS\_SCRIPT\_Security.gas`

3. Click **Save** (floppy disk icon or `Ctrl+S`)

4. Click **Deploy → New deployment**

5. Set **Type** to `Web app`

6. Set **Execute as** to `Me`

7. Set **Who has access** to `Anyone`

8. Click **Deploy** and authorize when prompted

9. Copy the **deployment URL** (looks like `https://script.google.com/macros/s/.../exec`)

### Step 3 — Connect the Frontend

1. Open `CompTIA-Security.html` in a text editor

2. Find the line with `GAS\_URL` near the top of the `\<script\>` section

3. Replace the placeholder value with your deployment URL from Step 2

4. Save the file


## Study Plan Overview

| Phase | Days | Topics |
| - | - | - |
| General Security Concepts | 1–18 | CIA Triad, Zero Trust, Cryptography, PKI, Identity & Access |
| Threats & Attacks | 19–30 | Malware, Social Engineering, Vulnerabilities, Network Attacks |
| Security Operations | 31–44 | Monitoring, Incident Response, Digital Forensics, SIEM |
| IRM & Governance | 45–54 | Risk Management, Compliance, Privacy, Third-Party Risk |
| Review & PBQ | 55–58 | Performance-based question practice, weak area review |
| Final Audit | 59–60 | Full mock exam conditions, exam-day checklist |



## Tech Stack

- **Frontend**: Vanilla HTML/CSS/JS — zero dependencies, no build step

- **Fonts**: DM Sans, DM Serif Display, DM Mono (Google Fonts)

- **Backend**: Google Apps Script (Web App deployment)

- **Storage**: `localStorage` (offline) + Google Sheets (cloud sync)


## License

MIT — free to use, modify, and share.


*Built to pass Security+ SY0-701. Good luck! 🔐*

