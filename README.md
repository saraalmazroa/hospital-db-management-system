# Dr. Soliman Fakeeh Hospital — Database Management System

A relational database project for **IT222: Database Principles**, Department of Information Technology, King Saud University (Phase 3, 2nd Semester 1447H).

A centralized DBMS that streamlines Dr. Soliman Fakeeh Hospital's daily operations — patient registration, appointment scheduling, medical records, and pharmacy inventory — built and deployed with an Oracle APEX front end.

## Team

- Najla Almazyad
- Ghala Alharbi
- Dana Alturaifi
- Sara Almazroa
- Wajd Alotaibi

Supervised by Tasneem Alowaisheq.

## Project Description

The system is used by hospital administrative and medical staff (receptionists, nurses, doctors) to register patients, schedule appointments, record diagnoses and treatments, manage admissions/discharges, and track pharmacy inventory.

## Core Entities

- **Doctor** — DoctorID (PK), Name, Specialization, RoomNum, Dept_code (FK)
- **Patient** — FileNumber (PK), NationalID, DOB, Gender
- **Department** — Dept_code (PK), Dept_Name, Location, ContactNo
- **Appointment** — APP_ID (PK), APP_Date, APP_Time, Status, DoctorID (FK), FileNumber (FK), Dept_code (FK)
- **Medicine** — CommercialName (PK), Price, Expiry_Date, Quantity

## Relationships

- Department 1:* Doctor
- Department 1:* Appointment
- Patient 1:* Appointment
- Doctor *:1 Appointment
- Doctor *:* Medicine (via `Prescribes` junction table)
- Patient *:* Medicine (via `Takes` junction table)

## What's Included

- Enhanced Entity-Relationship (EER) diagram and relational schema
- Full data dictionary (entities, relationships, attributes)
- DB table creation and data insertion scripts
- Sample SQL queries (e.g. find doctors by department, check medicine stock, insert appointments)
- Oracle APEX application: Interactive Grid (CRUD on all entities) and Master-Detail views (Department → Doctors)

## Work Distribution

| Task | Member |
|---|---|
| Data Queries | Najla Almazyad |
| App Builder | Ghala Alharbi |
| Table Creation | Dana Alturaifi |
| App Builder | Sara Almazroa |
| Data Insertion | Wajd Alotaibi |

## Files

- [`DB Project - Phase 3.pdf`](./DB%20Project%20-%20Phase%203.pdf) — full project report (requirements, EER diagram, schema, data dictionary, SQL, APEX build)
- [`DB_Phase3_Presentation.pdf`](./DB_Phase3_Presentation.pdf) — presentation slides

*Note: student ID numbers have been removed from both files before publishing.*
