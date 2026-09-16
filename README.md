# Emergency Health Record Wallet (EHRW)

> **"Your Medical History. Available When It Matters Most."**

[![Hackathon Prototype](https://img.shields.io/badge/Hackathon-Ready-emerald)](https://github.com)
[![Role-Based Access](https://img.shields.io/badge/Access-Role%20Based-blue)](https://github.com)
[![Audit Logged](https://img.shields.io/badge/Audit-Logged-purple)](https://github.com)

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
-

## 🔑 Pre-Configured Demo Accounts 

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

## 🌟 

## 📜 License
Healthcare Hackathon Prototype. Open for emergency reference software research.
use
