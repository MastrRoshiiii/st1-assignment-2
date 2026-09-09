SmartCare v0.2 - Requirements Specification Template

# Problem and Scope

SmartCare is a small clinic that is currently using a paper-based system that includes spreadsheets, paper records and manual processes to manage patients and appointments. The current system has shown to be inadequate, causing problems such as double bookings, finding patient records difficult, inconsistent appointment statuses and locating patients' records. The clinics management wants a small and easy to maintain software system to improve these processes and streamline operations.

# 2\. Stakeholders

| Stakeholder       | Need                                                                | Evidence                                                                                                                                                                         |
| ----------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Patients          | Reliable booking process                                            | Brief outlines wanting a system to support patient management.                                                                                                                   |
| Receptionists     | A streamlined process for appointment bookings                      | Several problems receptionists face have been outlined in the brief such as inconsistent appointment status, difficulty locating patient records, manual cancellation processes. |
| Practitioners     | Easy access to their appointment schedule and patients' information | Clinic management wants a simple software system to support practitioner management.                                                                                             |
| Clinic management | Reliable operation reports                                          | Clinic management faces difficulty producing basic operations reports.                                                                                                           |
| Developers        | Clear requirements and scope                                        | Brief outlines wanting a simple and easy to use software system to replace the paper based system.                                                                               |

# 3\. Functional Requirements

- **FR-01:** The system will allow the receptionist to create a new patient record.
- **FR-02:** The system will allow staff to search for a patient by patient name or ID.
- **FR-03:** The system will allow staff to view patient information.
- **FR-04:** The system will show practitioner availability.
- **FR-05:** The system will allow the receptionists to book an appointment for a patient.
- **FR-06:** The system will prevent the receptionists from booking an appointment when the selected practitioner is already unavailable at that time.
- **FR-07:** The system will allow staff to cancel an appointment.
- **FR-08:** The system will allow staff to update the status of an appointment.
- **FR-09:** The system will record cancelled appointments in the appointment history.
- **FR-10:** The system will allow staff to view appointment history.
- **FR-11:** The system will allow the receptionists and practitioners to view scheduled appointments.

# 4\. Non-Functional Requirements

- **NFR-1: Reliability:** The system will maintain accurate appointment history.
- **NFR-2: Maintainability:** The system should be simple for staff to understand and use and allow for changes to be made without redesigning the entire system.
- **NFR-3: Usability:** The system should have an easy-to-use interface.
- **NFR-4: Data Integrity:** The system will maintain patients' data and appointment information.

# 5\. User Stories

- **US-1:** As a manager I want to view appointment information so that I can monitor clinic operations.
- **US-2:** As a Practitioner, I want to view my scheduled appointments so that I know which of my patients I need to see.
- **US-3:** As a receptionist, I want to book appointments so that patients can be scheduled with a practitioner.
- **US-4**: As a patient I want to book an appointment so that I can discuss my health concerns with a healthcare professional.

# 6\. Acceptance Criteria

- **Given** appointments have been recorded, **when** the manager views them, **then** the system will display the appointment information.
- **Given** I have scheduled appointments, **when** I view my appointments, **then** system will display my scheduled appointments.
- **Given** a practitioner is available, **when** I book an appointment, **then** the appointment is recorded.
- **Given** my appointment has been booked, **when** the appointment information is saved, **then** my appointment booking is recorded in the system.

# 7\. Assumptions and Open Questions

Assumptions can be made for some addition features that the clinic may find useful in their day-to-day operations, such as Patient IDs, SMS/email appointment reminders for patients, an online portal for patients to be able to make bookings from an app via a mobile device.

Open questions that require further enquiry with the client, clarification on vague terms used in the brief such "easy to use", "appointments should normally be easy to cancel", patient search should be fast".

# 8\. AI Requirements Review Record

| AI suggestion                   | Evidence?                                                               | Decision             | Reason                        | Verification                          |
| ------------------------------- | ----------------------------------------------------------------------- | -------------------- | ----------------------------- | ------------------------------------- |
| Patients receive SMS reminders. | No evidence has been provided by the client that this is a requirement. | Requires validation. | An optional useful feature.   | Needed.                               |
| Facial recognition login.       | No evidence provided for this feature.                                  | Declined.            | Not needed.                   | Not needed.                           |
| Online payment.                 | No evidence provided for this feature in the client brief.              | Declined.            | Out of scope.                 | Feature can be offered to the client. |
| AI recommends treatments.       | None.                                                                   | Declined.            | Out of scope, possible risks. | Not needed.                           |
| Search by patient ID            | Not outlined in the brief.                                              | Requires validation. | An optional useful feature.   | Needed.                               |