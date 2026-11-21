# Cliniq Health — Hospital Management System (HMS)

A role-based Hospital Management System web application built to streamline patient onboarding, conflict-free appointment scheduling, digital prescribing, and itemized billing with instant receipt generation.

**Live Application:** `https://cliniq-hms.netlify.app` *(update with your deployed Netlify URL)*

---

## Key Features & Requirements Traceability

| Requirement | Module / Capability | Implementation Highlights |
| :--- | :--- | :--- |
| **FR1** | Authentication & RBAC | Strict role-isolated login/logout across **Admin**, **Doctor**, **Staff**, and **Patient** portals with unauthorized cross-role access prevention and security audit logging. |
| **FR2** | Patient Registration | Authorized staff register patients with duplicate validation and automatic unique ID generation (`PAT-2026-XXX`). |
| **FR3** | Conflict-Free Scheduling | Real-time slot availability validation preventing double-bookings for doctors and patients across dates and time windows. |
| **FR4** | Digital Prescriptions | Doctors issue structured multi-medication prescriptions (`RX-XXXX`) linked directly to patient records and consultations. |
| **FR5** | Billing & Receipts | Itemized invoicing for consultations, lab tests, and medications with payment settlement and unique receipt reference numbers (`RCP-XXXX`). |
| **NFR1–NFR5** | Security, Integrity & UX | Role-isolated views, input validation checks, persistent browser storage (`localStorage`), responsive clinical dashboard UI, and interactive WebGL/Three.js hero visuals. |

---

## Portal Access Credentials (Demo Environment)

| Role | Username | Password | Permitted Scope |
| :--- | :--- | :--- | :--- |
| **Administrator** | `AHAD` | `ahad123` | System governance, user/role registry, and RBAC security audit logs |
| **Doctor** | `dr.sharma` | `doc123` | Assigned consultation schedule and digital prescription issuance |
| **Staff** | `staff.reception` | `staff123` | Patient registration, appointment scheduling, and invoice generation |
| **Patient** | `patient.demo` | `pat123` | Personal health records, appointment booking, prescriptions, and bill payments |

---

## Project Structure

```text
cliniq-hms/
├── index.html      # Complete single-page HMS application (UI, RBAC engine, clinical logic, 3D visuals)
└── README.md       # System documentation, requirements mapping, and deployment guide
