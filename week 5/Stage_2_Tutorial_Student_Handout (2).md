Assignment 2 Case Study

Stage 2 Tutorial From Problems to Requirements

Week 5 | 60 minutes

# Learning goals

- Analyse stakeholders.
- Distinguish functional and non-functional requirements.
- Recognise ambiguity and unsupported requirements.
- Define scope.
- Develop user stories and acceptance criteria.
- Critique AI-generated requirements.

# Activity 1 - Stakeholder Map

| Stakeholder          | Need                                                                                      | Potential conflict                                                                                                                                        |
| -------------------- | ----------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Patients             | Able to book appointments and update their personal information.                          | Patients may want to change their information or appointments easily, while receptionists may need to verify changes to keep records accurate.            |
| Receptionists        | To be able to book, cancel or modify existing appointments, update patients' information. | Receptionists may want flexibility to change appointments, while health practitioners need their schedules to remain accurate and avoid double bookings.  |
| Health practitioners | Easy access to their appointment schedule and patients' information and notes.            | Practitioners may want quick access to patient information, while clinic management may require privacy controls and limited access to sensitive records. |
| Clinic management    | Reliable operation reports, admin privileges.                                             | Management may want more control and detailed information, while receptionists and practitioners may prefer fewer restrictions and a simpler system.      |
| Developers           | Clear requirements and scope from the client.                                             | The client may want additional features, but developers need to keep the project small and manageable.                                                    |

# Activity 2 - Functional or Non-Functional?

**X** Functional □ Non-functional The system shall allow staff to cancel an appointment.

□ Functional **X** Non-functional The system should remain responsive for the course-scale dataset.

**X** Functional □ Non-functional The system shall retain cancelled appointments.

□ Functional **X** Non-functional Core business logic should be independently testable.

**X** Functional □ Non-functional The system shall search for a patient by ID.

# Activity 3 - Repair Ambiguous Requirements

The system should be easy to use.

- **Problem:** Easy to use is a subjective statement.
- **Clarification question:** What tasks should each of the users be able to complete easily?

Patient search should be fast.

- **Problem:** Does not specify how patients will be searched.
- **Clarification question:** Will this search be done by name or a unique ID?

The system should securely manage data.

- **Problem:** Does not specify what level of security measures are needed.
- **Clarification question:** What security requirements are needed such as access controls, user logins?

Appointments should normally be easy to cancel.

- **Problem:** Does not specify who can cancel appointments or what happens after a cancellation.
- **Clarification question:** Who can cancel appointments, and will this remain recorded.  
  <br/>

#

Activity 4 - AI Requirements Audit

Classify each suggestion: Confirmed / Assumption requiring validation / Unsupported / Out of scope.

| AI suggestion                             | Classification                   | Evidence / reason                                                                                                                                                           |
| ----------------------------------------- | -------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Patients receive SMS reminders.           | Assumption requiring validation. | No evidence to support this, however, is a common feature among many clinics to help with appointment management.                                                           |
| Facial recognition login.                 | Out of scope.                    | Not specifically stated as a requirement by the client.                                                                                                                     |
| Receptionists create appointments.        | Confirmed.                       | Receptionists will be required to make appointment bookings and managing the clinics appointment schedule.                                                                  |
| Online payment.                           | Out of scope.                    | Not specified by the client.                                                                                                                                                |
| Practitioners view schedules.             | Confirmed.                       | Double booking has been an issue for the client as well as a lack of appointment history, being able to view schedules will help practitioners manage their daily schedule. |
| AI recommends treatments.                 | Out of scope.                    | Not specified by the client. Can have potential risks involved.                                                                                                             |
| Cancelled appointments remain in history. | Assumption requiring validation. | Not specified by the client, however, a reasonable feature for patient records.                                                                                             |

# Exit question

Why is 'AI suggested it' not sufficient evidence for a requirement?

AI suggestions may be based on assumptions rather than the clinic's needs. Requirements are outlined by the stakeholders needs, and problems identified in the clinic's operations.