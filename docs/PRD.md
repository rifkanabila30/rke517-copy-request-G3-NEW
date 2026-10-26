# Mini-PRD: Requests for a Copy of a Medical Record

**Client:** Ibu Ratna, head of the medical records unit, Klinik Harapan (fictional)

## 1. Problem and goal

### Problem today

Every day patients and families come to the counter to ask for a copy of a medical record (for insurance, referral, or to keep). Requests are written in a paper ledger, so nobody can see which requests are waiting. Last month the ledger went missing for 2 days, and one patient came back 3 times because her copy was never ready. Some copies were also given out without a letter from the patient and without an ID check.

### Goal

Klinik Harapan has one app where every copy request is recorded, verified, approved or rejected, and tracked until the copy is collected, allowing patients to submit requests independently so they don't have to go back and forth to counter staff.

## 2. Users and scope

### Users

| User (role) | What they do in the app |
|---|---|
| Requester (patient) | Submits a request for a copy of their own record directly in the app, uploads the ID, and checks the status of the request. |
| Unit staff (counter and filing) | Counter: checks the ID and authority letter of walk-in requesters and enters their requests. Filing: gets a notification after approval, prepares the copy, and records who collected it. |
| Head of medical records unit (Ibu Ratna) | The only person who approves or rejects a request. Writes a reason when rejecting. |

### In scope

- The app will record every copy request and replace the paper ledger (also requests sent directly by patients).
- The app will check ID and authority documents (KTP, authority letter, family card) before the head decides; the head approves or rejects with a reason.
- The app will show the status of each request: Pending/Waiting, Approved, Refused/Rejected, Ready, and Collected/Complete, and record who collected the copy and when.

### Out of scope

- The app will not handle payment or fees for copies (**our assumption**).
- The app will not store or edit the content of the medical record itself (**our assumption**).
- The app will not send the copy by post, courier, or email (**our assumption**).

## 3. User stories

| ID | As a… | I want… | So that… |
|---|---|---|---|
| US-1 | Patient / Family member | to submit a copy request directly through the app with required ID uploads | I can request copies remotely without making unnecessary trips to the counter. |
| US-2 | Counter staff | to verify uploaded identity and authority documents against requester details | I can prevent unauthorized persons from obtaining confidential medical records. |
| US-3 | Medical records unit | to approve or refuse requests with a logged refusal reason | I can legally control all record releases and maintain full auditability. |

## 4. Checks: how we will know it works

*Situation → Action → Result*

| ID | Situation (Given) | Action (When) | Result (Then) |
|---|---|---|---|
| C-1 | Patient RM-000123 requests a discharge summary copy with a valid KTP attached. | Head of Medical Records approves request REQ-2026-001. | Status changes to “Approved”, filing staff receives notification, and deadline is set to 3 working days. |
| C-2 | Requester R-202 submits a request for patient RM-000456 without attaching a signed Letter of Authority or requester's KTP. | Counter staff / System reviews the submitted documents. | Request is flagged as “Refused”, no preparation task is sent to filing staff, and system logs reason: “Missing Letter of Authority and Requester KTP”. |

## 6. Open questions for the client

| # | Question | Why it matters |
|---|---|---|
| 1 | Will approved medical record copies be provided as physical copies, digital copies, or both? | This determines which preparation and handover processes the application needs to support. |
| 2 | What exact statuses should the app show, and is there a time limit for the head to decide? She only said 3 working days after approval. | “Fast” is only defined after approval. Patients also need a clear status and a promised time before approval. |
