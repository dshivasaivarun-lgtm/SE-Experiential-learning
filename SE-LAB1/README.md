# Lab 1 — Requirements Engineering & UML Use-Case Modelling

**Course:** PES University — Dept. of Computer Science & Engineering
**Problem Statement #23** — Smart Cities, Transport & Logistics
**Title:** Hyperlocal Courier Dispatch & Tracking Engine

**Author:** Dharoor Shiva Sai Varun


**SRN:** PES1UG24CS150

---

## 📌 Problem Overview

An on-demand package delivery platform that assigns local parcel pickups to the nearest
delivery rider, optimizes multi-stop routing, and enforces OTP verification at the
destination.

**Actors:** Sender Client · Delivery Rider · Recipient

---

## 📂 Repository Contents

| File | Description |
|---|---|
| [`Requirements_table.docx`](./Requirements_table.docx) | Software Requirements Specification — Introduction, Overall Description (actors, assumptions, constraints), 5 Functional + 2 Nonfunctional Requirements table, Requirements Traceability Matrix, Glossary. |
| [`uml-diagram.drawio.pdf`](./uml-diagram.drawio.pdf) | UML Use-Case Diagram (draw.io export) — all actors, all 9 use cases, «include» and «extend» relationships. |
| [`UseCase_Model.pdf`](./UseCase_Model.pdf) | Companion use-case model: actor profiles, a full brief description for every use case (primary/secondary actor, trigger, precondition, description, related requirement), «include»/«extend» justification, and the diagram itself. |
| [`UseCase_Flow_Specification.pdf`](./UseCase_Flow_Specification.pdf) | One-page flow spec for *Complete Delivery with OTP Verification* (UC-05/UC-06) — Preconditions, Postconditions, Main Success Scenario, Alternate Flow. |

---

## ✅ Requirements Summary

| Req ID | Type | Priority | Summary |
|---|---|---|---|
| FR-001 | Functional | High | Match request to nearest active rider within 3 km |
| FR-002 | Functional | High | Sender creates a delivery request |
| FR-003 | Functional | High | Rider accepts/rejects dispatch; auto-reassign |
| FR-004 | Functional | High | OTP generation & validation at delivery |
| FR-005 | Functional | Medium | Multi-stop route optimization |
| NFR-001 | Nonfunctional | High | Live telemetry latency < 2 seconds |
| NFR-002 | Nonfunctional | High | Encryption of OTP & GPS data |

Full descriptions, acceptance criteria, and rationale are in `Requirements_table.docx`.

---

## 🧩 Use-Case Model Summary

9 use cases (UC-01 – UC-09) covering request creation, rider matching, dispatch
accept/reject, route optimization, OTP-verified delivery completion, live tracking, delay
reporting, and post-delivery feedback.

- **«include»**: `Create Delivery Request` → `Match Nearest Rider`; `Complete Delivery` → `Verify OTP`
- **«extend»**: `Report Delivery Delay` extends `Track Delivery Status`

See `UseCase_Model.pdf` for full use-case descriptions and `uml-diagram.drawio.pdf` for the diagram.

---

## 🛠 Tools Used

- draw.io — UML Use-Case Diagram
- Microsoft Word (.docx) — SRS and flow specification
