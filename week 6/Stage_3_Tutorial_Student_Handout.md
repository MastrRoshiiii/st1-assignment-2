Assignment 2-Case Study

Stage 3 Tutorial Activities

From Requirements to Domain Models

Week 6 | 60 minutes

# Candidate Concepts

| Candidate    | Class? | Reason                                                                          |
| ------------ | ------ | ------------------------------------------------------------------------------- |
| Patient      | Yes    | Patient is a class as it has its own ID, Attributes as well as Behaviours.      |
| Practitioner | Yes    | Practitioner is a class as it has its own ID, Attributes as well as Behaviours. |
| Appointment  | Yes    | Appointment is a class as it has its own ID, Attributes as well as Behaviours.  |
| Name         | No     | Name is a piece of data.                                                        |
| Clinic       | No     | Not needed.                                                                     |
| Database     | No     | This is a technology, not a concept of a clinic.                                |
| Cancellation | No     | Is an event, not a Class.                                                       |
| Status       | No     | Is an Attribute, not a Class.                                                   |

# CRC Cards

## Patient

| Class: Patient                     |                   |
| ---------------------------------- | ----------------- |
| Responsibilities                   | **Collaborators** |
| Know own ID, name, contact details | N/A               |
| Provide/view own information       | Receptionist      |
| Update own information             | Receptionist      |

## Practitioner

| Class: Practitioner                          |                           |
| -------------------------------------------- | ------------------------- |
| Responsibilities                             | **Collaborators**         |
| Know own ID, name, schedule                  | N/A                       |
| Check own availability at a given time       | Receptionist, Appointment |
| Provide a list of own scheduled appointments | Receptionist, Appointment |
| Update appointment status                    | Receptionist, Appointment |

## Appointment

| Class: Appointment                                             |                            |
| -------------------------------------------------------------- | -------------------------- |
| Responsibilities                                               | **Collaborators**          |
| Hold and report own ID, date/time, status                      | N/A                        |
| Hold reference to which Patient and Practitioner it belongs to | Patient, Practitioner      |
| Apply a status change when instructed (cancelled, completed)   | Receptionist, Practitioner |

# Relationship Reasoning

Patient to Appointment: which relationship and why?

- Association, not inheritance. Patient and Appointment are linked by a reference, not classified as a "is-a" relationship. An Appointment has a Patient, an Appointment "is not a" Patient.

Practitioner to Appointment: what multiplicity?

- 1 — 0..\* — one Practitioner can have many appointments or none yet, but each Appointment has exactly one Practitioner.

Should Appointment inherit from Patient?

- No. Inheritance means "is-a", an Appointment is not a type of Patient. It references a Patient.

Does Clinic need to own every object?

- No. Objects already reference each other without the need for a parent. This would create clinic as a "god class".

# AI Model Critique

Critique AI proposals: PatientManager, PractitionerManager, AppointmentManager, ClinicController, NotificationManager, ScheduleEngine.

All six proposal are rejected. PatientManager, PractitionerManager, AppointmentManager duplicate responsibilities that have already been assigned to the Classes Patient, Practitioner and Appointment. ClinicController would introduce the "god class" and is unnecessary for the clinics requirements. NotificationManager is not outlined as a requirement, notifications are a feature that is still pending review as an assumption for a useful feature. ScheduleEngine already has a solution with the bookAppointment() method that _calls_ the checkAvailability() method.