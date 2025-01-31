CREATE DATABASE Healthcare;
USE Healthcare;
CREATE TABLE Patients (
    patient_id INT PRIMARY KEY AUTO_INCREMENT,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    date_of_birth DATE,
    gender VARCHAR(10),
    phone_number VARCHAR(15),
    address VARCHAR(100)
);
INSERT INTO Patients (first_name, last_name, date_of_birth, gender, phone_number, address)
VALUES ('John', 'Doe', '1990-05-15', 'Male', '123-456-7890', '123 Main St');
SELECT * FROM Patients;
SELECT a.appointment_id, p.first_name, p.last_name, a.appointment_date, a.appointment_time
FROM Appointments a
JOIN Patients p ON a.patient_id = p.patient_id
WHERE a.doctor_id = 1;
SELECT m.diagnosis, m.treatment, m.date_of_visit, d.first_name AS doctor_first_name, d.last_name AS doctor_last_name
FROM Medical_History m
JOIN Doctors d ON m.doctor_id = d.doctor_id
WHERE m.patient_id = 1;
UPDATE Billing
SET payment_status = 'Paid'
WHERE bill_id = 1;
DELETE FROM Patients
WHERE patient_id = 1;
SELECT b.bill_id, p.first_name, p.last_name, b.bill_amount, b.bill_date
FROM Billing b
JOIN Patients p ON b.patient_id = p.patient_id
WHERE b.payment_status = 'Unpaid';
