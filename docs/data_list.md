# Data list

The Week 6 Mini-PRD PDF labels this section “What must the app keep? (6 fields)”. The table in that source contains seven rows, reproduced below.

| Field name | Meaning | Example | Required? | Rule |
|---|---|---|---|---|
| `request_id` | Unique number of the request | `REQ-0001` | Y | Every request must have a unique ID. (Our assumption: the system generates the ID automatically.) |
| `patient_mrn` | The patient's medical record number | `RM-000123` | Y | Must match the patient whose record copy is requested. |
| `requester_identity` | Identity details of the person submitting the request | KTP checked | Y | The requester's identity must be checked. |
| `relationship_authority` | The requester's relationship to the patient and evidence of authorization | Patient's child; signed authorization letter | When applicable | Family members must provide the requester's KTP, the patient's KTP, and a signed authorization letter. For children under 17, a parent must provide the Family Card (KK), based on the interview. |
| `document_requested` | The type of medical record document requested | Discharge summary | Y | The requested document type must be clearly recorded. |
| `decision_status_collection` | The decision, request status, and collection information | Approved; copy collected | Y | Only the Head may approve or reject requests. Rejection reasons and collection details must be recorded. |
| `Collection record` | When the copy was collected, by whom, and which staff handed it over | 8 Oct 2026, example; Patient (Budi), approved by staff Rina | Y | Must be recorded before the request can be marked complete. |
