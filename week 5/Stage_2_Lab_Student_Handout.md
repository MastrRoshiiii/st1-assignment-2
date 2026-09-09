Assignment 2 – Case Study Lab

Stage 2 Lab Activities

SmartCare Requirements Engineering

AI OFF -> AI ON -> VERIFY | 1 hour

# Learning objectives

- Analyse the SmartCare client brief.
- Identify stakeholders and scope.
- Write functional and non-functional requirements.
- Develop user stories and Given-When-Then acceptance criteria.
- Use AI to critique requirements without allowing it to invent stakeholder needs.
- Produce SmartCare Requirements Specification v1.0.

# Part A - Client Brief: AI OFF

SmartCare uses spreadsheets and paper records. Staff report duplicate bookings, difficulty finding patient information, inconsistent appointment status and limited appointment history. Management wants a small, maintainable patient, practitioner and appointment system.

- SmartCare is a small clinic that is currently using a paper-based system that includes spreadsheets, paper records and manual processes to manage patients and appointments. The current system has shown to be inadequate, causing problems such as double bookings, finding patient records difficult, inconsistent appointment statuses and locating patients' records. The clinics management wants a small and easy to maintain software system to improve these processes and streamline operations.

# Part B - Stakeholders and Scope: AI OFF

Identify at least four stakeholders. Create In Scope and Out of Scope lists. Label uncertain features as provisional rather than confirmed.

**Stakeholders:**

1. **Clinic Management**
2. **Healthcare Practitioners**
3. **Receptionists**
4. **Patients**

**In Scope:**

- Patient management
- Practitioner management
- Appointment management
- Booking appointments
- Cancelling appointments
- Searching for patient information
- Managing appointment status
- Maintaining appointment history
- Preventing double booking appointments

**Out of Scope:**

- Billing and payments
- Prescription processes
- AI assisted patient diagnosis or treatment management
- SMS/email notification systems

**Provisional Features:**

The clinic may find these features useful

- **Online portal access for patients** – Provisional
- **SMS/email appointment reminders** – Provisional
- **Online patient self-booking** – Provisional

# Part C - Functional Requirements: AI OFF

Write 8-12 numbered functional requirements using FR-01, FR-02 and so on. Each should describe one observable capability.

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

# Part D - Non-Functional Requirements: AI OFF

Write 4-6 numbered non-functional requirements covering appropriate qualities such as reliability, maintainability, usability, data integrity or testability.

- **NFR-1: Reliability:** The system will maintain accurate appointment history.
- **NFR-2: Maintainability:** The system should be simple for staff to understand and use and allow for changes to be made without redesigning the entire system.
- **NFR-3: Usability:** The system should have an easy-to-use interface.
- **NFR-4: Data Integrity:** The system will maintain patients' data and appointment information.

# Part E - User Stories and Acceptance Criteria: AI OFF

Write 4-6 user stories. For at least three, create Given-When-Then acceptance criteria including one negative or failure scenario.

- **US-1:** As a manager I want to view appointment information so that I can monitor clinic operations.
  - **Given** appointments have been recorded, **when** the manager views them, **then** the system will display the appointment information.
- **US-2:** As a Practitioner, I want to view my scheduled appointments so that I know which of my patients I need to see.
  - **Given** I have scheduled appointments, **when** I view my appointments, **then** system will display my scheduled appointments.
  - **Given** I have no scheduled appointments, **when** I view my appointments, **then** the system will indicate that I have no scheduled appointments.
- **US-3:** As a receptionist, I want to book appointments so that patients can be scheduled with a practitioner.
  - **Given** a practitioner is available, **when** I book an appointment, **then** the appointment is recorded.
  - **Given** a practitioner already has an appointment at that time, **when** I try to book another appointment, **then** the system prevents the duplicate booking.
- **US-4**: As a patient I want to book an appointment so that I can discuss my health concerns with a healthcare professional.
  - **Given** my appointment has been booked, **when** the appointment information is saved, **then** my appointment booking is recorded in the system.
  - **Given** my appointment has been cancelled, **when** the appointment status is updated, **then** the cancelled appointment remains in the appointment history.

# Part F - AI Requirements Review: AI ON

Prompt: Act as a software requirements reviewer. Review the SmartCare requirements for ambiguity, inconsistency, missing clarification questions and testability. Do NOT invent new client requirements. For every suggestion, state whether it is based on evidence or is only a question/assumption requiring validation.

# AI Response

**Part F – AI Requirements Review**

| **Requirement / Area**                   | **Review / Suggestion**                                                                                                      | **Evidence or Validation?**                                                                                                                             |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FR-01: Create a patient record**       | Clarify what minimum information is required when creating a patient record.                                                 | **Question requiring validation** – the brief confirms patient management but does not specify required fields.                                         |
| **FR-02: Search by patient ID**          | This is clear and testable, but confirm that patient ID is the required search method.                                       | **Evidence** – searching for patient information is supported by the brief; the specific use of ID should be validated.                                 |
| **FR-07: Prevent duplicate bookings**    | Define what counts as a duplicate booking, such as the same practitioner, date and time.                                     | **Evidence** – duplicate bookings are an identified problem in the client brief. The exact definition requires validation.                              |
| **FR-08: Cancel an appointment**         | Clarify who is allowed to cancel an appointment and what happens to the appointment after cancellation.                      | **Evidence** – manual cancellation is identified as a problem. The specific cancellation rules require validation.                                      |
| **FR-09: Update appointment status**     | Define which appointment statuses are required, such as booked or cancelled.                                                 | **Evidence** – inconsistent appointment status is identified in the brief. The exact status values require validation.                                  |
| **FR-10: Retain cancelled appointments** | This supports the need for reliable appointment history, but the required length of time for retaining records is unclear.   | **Evidence** – limited appointment history is identified as a problem. Retention duration requires validation.                                          |
| **NFR-01: Reliability**                  | "Normal clinic operating hours" is ambiguous and should be defined.                                                          | **Question requiring validation** – the brief does not specify operating hours or availability targets.                                                 |
| **NFR-03: Usability**                    | "Clear and consistent" is subjective. A measurable usability criterion would need to be agreed with the client.              | **Question requiring validation**.                                                                                                                      |
| **NFR-04: Data Integrity**               | "Conflicting appointment records" should be clearly defined so it can be tested.                                             | **Evidence** – duplicate bookings and inconsistent appointment information are problems in the brief; the exact validation rules require clarification. |
| **NFR-05: Testability**                  | The requirement is reasonably clear, but the specific business logic that must be independently tested should be identified. | **Evidence** – maintainability is explicitly requested; the exact testing scope requires validation.                                                    |

**Overall Review**

The SmartCare requirements generally match the client brief, particularly around patient, practitioner and appointment management, duplicate bookings, appointment status and appointment history. Some requirements contain ambiguous terms such as **"easy," "reliable," "normal," and "clear."** These should be clarified or made measurable before implementation. The client brief provides evidence for the identified problems, but it does not provide enough information to confirm details such as required patient fields, appointment status values, cancellation rules, retention periods or clinic operating hours. These should therefore be treated as **clarification questions rather than new requirements**.

This directly addresses the instruction **"Do NOT invent new client requirements"** because you're identifying what needs clarification rather than deciding the answers yourself.

# Part G - VERIFY the AI Review

Classify each significant AI suggestion as Accepted, Modified, Rejected, or Unverified. Explain the evidence used.

| AI Suggestion:                                         | Classification: | Evidence:                                                                                                          |
| ------------------------------------------------------ | --------------- | ------------------------------------------------------------------------------------------------------------------ |
| Clarify required patient information                   | Unverified      | The brief says patient management is needed but does not specify the required fields.                              |
| Confirm patient ID as the search method                | Unverified      | The brief mentions difficulty finding records but does not specifically require searching by ID.                   |
| Define what counts as a double booking                 | Accepted        | Double bookings are identified as a current problem.                                                               |
| Clarify who can cancel appointments                    | Unverified      | Manual cancellation is identified but it does not specify who can perform this task.                               |
| Define appointment statuses                            | Accepted        | Inconsistent appointment status is identified as a problem in the brief.                                           |
| Clarify appointment retention period                   | Unverified      | The brief requires better appointment history but does not specify how long records should be kept.                |
| Define "normal clinic operating hours"                 | Modified        | The brief does not specify operation hours.                                                                        |
| Make usability measurable                              | Modified        | Maintainability is requested, but "clear and consistent" is subjective and will need to be verified by the client. |
| Define "conflicting appointment records"               | Accepted        | This suggestion relates directly with the problem of double bookings.                                              |
| Identify business logic that needs independent testing | Unverified      | The brief does not describe which logic must be tested.                                                            |

# Part H - Finalise SmartCare v0.2

Submit stakeholder analysis, scope, 8-12 FRs, 4-6 NFRs, 4-6 user stories, acceptance criteria, assumptions/open questions and selected AI review evidence.

# Reflection

In 150-250 words: What did AI notice that you missed? What did AI invent or overreach on? Which requirement changed after review? Why must requirements have evidence?

AI was able to notice that some of the requirements were too vague and needed clarification such as "reliable" and "clear". These could be interpreted differently.

AI also overreached as it generally does by suggesting details that were not outlined in the brief by the client such as using a patient ID for patient identification and a search method, who should be allowed to cancel appointments without clarifying and how long cancelled appointments should remain in the patients records. These were assumptions that require verification.

Requirements must have evidence because they should reflect what was outlined in the brief by the client and stakeholders. Without evidence of these requirements, developers could build features that the clinic does not need or want in their system. Evidence helps to keep the requirements relevant to the scope. AI can help identify problems with requirements, but it should not be treated as evidence for what the client needs.