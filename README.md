# Data Modeling for a Hospital Management System

This project outlines the data modeling approach for a hospital management system. It serves as a blueprint for the system's database structure, ensuring efficient data storage, retrieval, and manipulation of hospital information.

# Components
The data model consists of several key components:

### Entity-Relationship Diagram (ERD):

A visual representation of the system's entities (data objects) and their relationships. Common entities include:
Patient (attributes: Patient_ID, Name, Age, Disease, Room_Number)
Doctor (attributes: Doctor_ID, Name, Specialization)
Nurse (attributes: Nurse_ID, Name, Salary)
Ward_Boy (attributes: Ward_Boy_ID, Name, Description, Salary)
Room (attributes: Room_Number, Room_Type, Status)
Appointment (attributes: Appointment_ID, Date, Time, Doctor_ID, Patient_ID)
The ERD depicts relationships between entities, such as:
A patient is assigned to a room (one-to-one).
A doctor has many appointments (one-to-many).
A nurse can be responsible for multiple rooms (one-to-many).


### Enhanced Entity-Relationship (EER) Model:

An extension of the ERD that provides further details about relationships. It might include:
Specialization (e.g., Surgeon, Cardiologist subtypes of Doctor).
Generalization (e.g., Staff supertype for Nurse and Ward_Boy).
Cardinalities (specific relationship occurrences, e.g., one-to-one, one-to-many, many-to-many).

### Relational Schema:

A structured representation of the database tables corresponding to the ERD/EER model entities. The schema defines:
Tables (entities).
Columns (attributes) and their data types.
Constraints (primary and foreign keys) to enforce data integrity and relationships.
Example table structure:
Patient table:
  - Patient_ID (INT, Primary Key)
  - Name (VARCHAR)
  - Age (INT)
  - Disease (VARCHAR)
  - Room_Number (INT, Foreign Key referencing Room.Room_Number)

    
### Business Rules:

Specific rules governing data management within the system, ensuring data integrity and consistency. Examples:
A patient must be assigned a room before an appointment can be scheduled.
A doctor can have multiple appointments in a day.
A nurse can be assigned to multiple rooms.
