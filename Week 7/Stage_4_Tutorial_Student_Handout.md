Assignment 2 – Case Study

Stage 4 Tutorial Activities

Object-Oriented Design Decisions

Week 7 | 60 minutes

# Activity 1 - Encapsulation Review

| Class        | Protected state / invariant                            | Public operations                               |
| ------------ | ------------------------------------------------------ | ----------------------------------------------- |
| Patient      | patientID, name, contactDetails                        | viewInfo(), updateInfo()                        |
| Practitioner | PractitionerID, name, schedule                         | checkAvailability(), getScheduledAppointments() |
| Appointment  | appointmentID, dateTime, status, patient, practitioner | cancel(), updateStatus()                        |

# Activity 2 - Composition or Inheritance?

Appointment and Patient -> ✓ Composition/association **X** Inheritance. Reason: An _Appointment_ has a _Patient_. An _Appointment_ references a _Patient._

Appointment and Practitioner -> ✓ Composition/association **X** Inheritance. Reason: An _appointment_ has a _practitioner_.

Doctor and Practitioner (hypothetical) -> **X** Composition/association ✓ Inheritance. Reason: A _Doctor_ is a specific type of _Practitioner_ and inherits _Practitioners_' attributes/behaviours.

Clinic and Appointment -> ✓ Composition/association **X** Inheritance. Reason: A _Clinic_ could hold a collection of _Appointments_, but an _Appointment_ is not a type of _Clinic_.

# Activity 3 - Responsibility Allocation

Who decides whether SCHEDULED can become CANCELLED?

- The Appointment classes decides this as it owns the status attribute and its own updateStatus() method.

Who validates a patient name?

- The Patient themselves. They provide the name the Patient class uses during their registration.

Should Appointment execute SQL? Why?

- No. Classes should not contain databases or technical logic directly.

Should the UI decide whether a status transition is legal?

- No. Only classes that have the permissions to updateStatus() should have this decision.

# Activity 4 - AI Code Critique

AI generates an Appointment class with public status mutation, SQL inside cancel(), a NotificationManager dependency and inheritance from PatientRecord. Identify at least five design problems and corrections.

1. **Public Status Mutation**:

- Anyone could change the status directly with no checks in place. That is why we have the methods like cancel() and updateStaus() in place to validate these changes are correct.

1. **SQL Inside Cancel**:

- Mixing database code into the Appointment class would be tangling business rules and data storage together. Keep database code separate. Appointment should update its own info, not talk directly to the database.

1. **NotificationManager Dependency**:

- Reminders are not confirmed yet by the client and are out of scope for the requirements. If this is to be approved, they should be handled separately instead of built into Appointment class.

1. **Inheritance from PatientRecord**:

- An Appointment is not a type of Patient. It only needs to know which Patient it is for. Appointment should only hold a reference to Patient, not inherit from it.

1. **No check on valid status changes**:

- With a public status and SQL inserted into cancel(), no checks are in place for illegal changes such as Cancelled changing back to Scheduled. The check should be inside Appointments methods so it can validate before changing its status.

# Exit question

Why can code be object-oriented syntactically but still have poor object-oriented design?

Using OOP syntax like (classes, inheritance) doesn't guarantee OOP principles (encapsulation, single responsibility, correct relationships) are followed correctly. You can write object-oriented code that ticks all the boxes but still has a badly designed model as seen in activity 4.