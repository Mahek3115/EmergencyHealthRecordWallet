# Emergency Health Record Wallet (EHRW)

> **"Your Medical History. Available When It Matters Most."**

[![Hackathon Prototype](https://img.shields.io/badge/Hackathon-Ready-emerald)](https://github.com)
[![Role-Based Access](https://img.shields.io/badge/Access-Role%20Based-blue)](https://github.com)
[![Audit Logged](https://img.shields.io/badge/Audit-Logged-purple)](https://github.com)

---

## 🚨 Hackathon Safety Disclaimer

> **IMPORTANT**: This is a healthcare record management prototype built for a hackathon. 
> The system **only stores, organizes, and displays patient-provided and hospital-provided medical records**. 
> It does **NOT** make medical diagnoses or treatment decisions.

---

## 🏥 Problem Statement & Solution

In traffic accidents and sudden medical emergencies, unconscious or critical patients cannot communicate their essential medical history. Family members may be unavailable or unaware of prior surgeries, drug allergies, or chronic conditions. Carrying bulky physical files is impractical.

**Emergency Health Record Wallet** solves this by providing:
1. **Digital Patient QR Wallet**: Fast access to critical emergency medical summaries (Blood Group, Penicillin/Drug Allergies, Active Conditions, Surgeries, Current Medicines, Emergency Contact).
2. **Secure Tokenized QR Access**: The QR code does **not** publicly expose full medical data. Approved hospitals scan the QR and must submit an authorized emergency access reason before viewing the summary.
3. **Automated History Timeline**: Finalized hospital treatment records automatically sync into the patient's visual medical timeline.
4. **Immutable Audit Trail**: Every emergency access attempt is recorded in a transparent audit log visible to patients and system administrators.

---

## 👥 User Roles & Capabilities

| Role | Access Privileges | Key Features |
| :--- | :--- | :--- |
| **PATIENT** | Full ownership of profile | • View Emergency QR & generate Lockscreen Badges<br>• View Medical Profile (Allergies, Conditions, Surgeries, Meds)<br>• Upload & categorize medical documents (scans, lab tests)<br>• Interactive visual Medical History Timeline<br>• Real-time Hospital Access Audit Log & Alerts |
| **HOSPITAL / DOCTOR** | Verified emergency access | • Search Patient by ID (`EHRW-2026-001245`) or QR Scanner<br>• Authorized Emergency Access Protocol (logs access reason)<br>• Fast Emergency Medical Summary with red critical allergy callouts<br>• Create Hospital Admission (`ADM-2026-XXXXX`)<br>• Add Treatment Records -> **Auto-updates Patient Timeline** |
| **SYSTEM ADMIN** | Platform governance | • Review pending hospital registration applications<br>• Approve, Reject, or Suspend hospital credentials<br>• Inspect system-wide audit logs and emergency accesses<br>• Platform security monitoring |

---

## 🔄 End-to-End Emergency Workflow

```
[ PATIENT ]
Register -> Generate Patient ID (EHRW-2026-001245) & QR Token
↓
Add Allergies, Surgeries, Medications & Documents
↓
Download Printable Emergency Wallet Card / Lockscreen Graphic

[ EMERGENCY EVENT ]
Accident occurs → Unconscious patient brought to ER
↓
[ APPROVED HOSPITAL ]
Scan Patient QR / Enter Patient ID
↓
System prompts for Mandatory Emergency Access Reason
(e.g., "Unconscious accident victim brought by ambulance")
↓
System logs event to Audit Trail & triggers Alert
↓
Renders EMERGENCY MEDICAL SUMMARY (Blood Group O+, Penicillin Allergy, Cardiac Surgery)
↓
Create Admission (ADM-2026-00981) → Perform Treatment & Procedures
↓
Finalize Treatment Record → AUTOMATICALLY APPENDS TO PATIENT'S TIMELINE
```

---

## ⚡ How to Run Locally

### Prerequisites
- Node.js (v18+) & npm

### Installation & Execution
```bash
# 1. Open project directory
cd C:\Users\user\.gemini\antigravity\scratch\emergency-health-wallet

# 2. Install dependencies (if not already installed)
npm install

# 3. Start local development server
npm run dev
```

Open `http://localhost:5173` in your browser.

---

## 🌐 How to Deploy to Production / Live Hackathon URL

### Production Build Command
First generate the static distribution bundle:
```bash
npm run build
```
This produces an optimized production bundle in the `dist/` directory.

---

### Option 1: Firebase Hosting (Recommended Free & Fast Deployment)

Firebase Hosting provides a free `https://<your-app>.web.app` domain with SSL.

```bash
# 1. Login to Firebase
npx -y firebase-tools@latest login

# 2. Initialize Firebase Hosting
npx -y firebase-tools@latest init hosting

# Configuration Answers:
# ? What do you want to use as your public directory? dist
# ? Configure as a single-page app (rewrite all urls to /index.html)? Yes
# ? Set up automatic builds and deploys with GitHub? No

# 3. Build & Deploy
npm run build
npx -y firebase-tools@latest deploy
```

---

### Option 2: Vercel (1-Click Deployment)

```bash
# Deploy using Vercel CLI
npx vercel
```
Follow the interactive prompts to get an instant `https://<your-project>.vercel.app` URL.

---

### Option 3: Netlify Drag & Drop / CLI

```bash
# Build the project
npm run build

# Deploy via Netlify CLI
npx netlify-cli deploy --prod --dir=dist
```
Or simply drag the `dist/` folder into [app.netlify.com/drop](https://app.netlify.com/drop).

---

### Option 4: GitHub Pages

```bash
# Install gh-pages dependency
npm install -D gh-pages

# Deploy to GitHub Pages
npx gh-pages -d dist
```

---

## 🔑 Pre-Configured Demo Accounts for Judges

Use the **Floating Presentation Switcher** at the bottom of the app to instantly toggle between demo accounts:

1. **Demo Patient**: `Rahul Patil`
   - **Patient ID**: `EHRW-2026-001245`
   - **Blood Group**: `O+`
   - **Emergency Contact**: Priya Patil (+91 98765 43210)
   - **Critical Allergy**: Penicillin (Life-Threatening)
   - **Surgeries**: Coronary Artery Bypass Graft (2023)

2. **Demo Approved Hospital**: `City Care Emergency Hospital`
   - **Hospital ID**: `HOSP-2026-0089`
   - **Status**: `APPROVED`
   - **Privileges**: Full Emergency Access & Admission privileges

3. **Demo Pending Hospital**: `Apex Metro Trauma Center`
   - **Hospital ID**: `HOSP-2026-0199`
   - **Status**: `PENDING`
   - **Privileges**: Locked emergency access pending Admin review

4. **Demo System Admin**: `System Admin`
   - **Privileges**: Hospital Verification, Approval Queue, Audit Log Console

---

## 🌟 Hackathon Highlights & Features

- **Multi-Language Support**: Instant UI toggle for **English**, **Hindi (हिंदी)**, and **Marathi (मराठी)**.
- **Printable Emergency QR Card**: Download or print wallet-sized emergency card with QR code and blood group badge.
- **Emergency Lockscreen Graphic**: Smartphone lockscreen wallpaper generator.
- **Interactive Visual Timeline**: Chronological medical history node visualization.
- **Local Persistence**: State automatically persists across page refreshes using `localStorage`.

---

## 📜 License
Healthcare Hackathon Prototype. Open for emergency reference software research.
