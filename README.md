# Hospital-Management

This **Hospital Management System** project implements a relational database schema designed to manage various operations within a hospital, including patient records, doctor schedules, appointments, diagnoses, and medical histories. The system leverages SQL to structure and enforce relationships between different entities, ensuring data integrity and efficient retrieval of information.

### Key Features:

1. **Patient Management**: 
   - The system records patient information, including personal details, medical history, and visit records.
   - Patients can have multiple visits, each tracked with related concerns, symptoms, and diagnoses.

2. **Doctor Management**: 
   - Doctors' personal details, schedules, and access to patient medical histories are managed within the system.
   - Doctors are linked to appointment schedules and can view and diagnose patient conditions.

3. **Appointment System**: 
   - A comprehensive appointment system tracks patient visits, schedules, and status updates.
   - Appointments are linked to both patients and doctors to ensure accurate tracking of medical consultations.

4. **Medical History**: 
   - A detailed medical history table records patients' past conditions, surgeries, and medications.
   - Doctors have the ability to access and view patient medical histories.

5. **Scheduling System**: 
   - A flexible schedule management system tracks doctors’ availability with start times, end times, and break periods for different days.

6. **Diagnosis and Prescription**: 
   - Doctors can record diagnoses and prescribe medication for patient visits, which are stored and linked with the respective appointments.

### Database Structure:

- **Schema**: All tables are organized within the `hospital_management` schema.
- **Entities**:
  - `patient`: Stores patient information such as email, password, name, address, gender.
  - `doctor`: Stores doctor information such as email, name, gender, and password.
  - `appointment`: Manages appointments with date, time, and status information.
  - `medical_history`: Tracks patient health records, surgeries, and medications.
  - `patient_visits`: Logs patient visits, concerns, and symptoms for each appointment.
  - `schedule`: Stores the working hours and breaks for each doctor.
  - `diagnose`: Records diagnoses and prescriptions made by doctors for specific appointments.
  - `doctor_schedules`: Links doctors with their schedules.
  - `doctor_view_history`: Tracks medical history viewed by doctors.

### Relational Design:

- **Primary and Foreign Keys**: 
  - Tables are interlinked using primary and foreign keys to ensure data consistency across patients, doctors, appointments, schedules, and medical histories.
  - Many-to-many and one-to-many relationships are handled using linking tables such as `patient_visits`, `diagnose`, and `doctor_schedules`.

- **Referential Integrity**: 
  - The schema enforces referential integrity by ensuring that foreign key relationships are maintained, such as linking appointments to patients and doctors, and medical histories to patients.

### Technologies Used:

- **PostgreSQL**: The schema is designed for PostgreSQL databases, taking advantage of features like foreign keys, cascading operations, and serial identifiers for auto-incrementing values.

### How to Use:

1. Clone the repository.
2. Execute the provided SQL schema to create the database and tables.
3. Populate the tables with patient, doctor, and appointment data.
4. Utilize the system for hospital management tasks like scheduling, diagnosing, and viewing patient medical histories.

This project is intended to serve as a foundation for hospital management systems and can be extended with additional features like billing, reporting, and patient-doctor messaging.

