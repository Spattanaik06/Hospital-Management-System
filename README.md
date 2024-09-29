# Hospital-Management-System
Hospital Management System
Project Overview
The Hospital Management System is a Java-based application designed to manage patient and doctor information, as well as to facilitate the booking of patient appointments. This system allows hospital staff to perform essential tasks such as adding and viewing patients, viewing doctors, and booking appointments. The application connects to a MySQL database to store and retrieve data, ensuring secure and efficient data management.

Features
Add Patient: Allows staff to add new patients to the system by capturing essential details such as name, age, gender, and mobile number.

View Patient: Displays a list of all registered patients, along with their details (ID, name, age, gender, and mobile number).

View Doctor: Lists all available doctors, including their ID, name, and department.

Book Appointment: Enables booking of appointments for patients with a specific doctor on a selected future date.

Exception Handling: The system includes validation to prevent users from booking appointments on the current date or any past date. If such an attempt is made, an exception (InvalidAppointmentDateException) is thrown, informing the user that appointments must be booked for future dates only.
Exit: Safely exits the application.

Technologies Used
Java: Core language used for developing the application.
MySQL: Database used for storing patient, doctor, and appointment details.
JDBC: Java Database Connectivity (JDBC) is used to connect the application to the MySQL database.
Exception Handling: Custom exception handling is implemented to manage invalid inputs (e.g., booking an appointment on a past date).

Database Structure
The system relies on the following MySQL database schema:

Tables:

Patients:
PatientId (INT, Primary Key, Auto Increment)
PatientName (VARCHAR)
Age (INT)
Gender (VARCHAR)
MobileNo (VARCHAR)


Doctors:
DoctorId (INT, Primary Key, Auto Increment)
DoctorName (VARCHAR)
Department (VARCHAR)


Appointments:
AppointmentId (INT, Primary Key, Auto Increment)
PatientId (INT, Foreign Key)
DoctorId (INT, Foreign Key)
AppointmentDate (DATE)
