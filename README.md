# doctors_appointment

# Appointment Management System

## Overview

This is a simple appointment management system implemented using FastAPI and SQLite. The system allows doctors to create appointments for their patients and manage their schedules efficiently.

## Features

- Create and manage doctor profiles with specialties, maximum patient capacity, practice locations, and practice times.
- Book appointments for patients, ensuring that doctors are available and not overbooked.
- Validate appointment dates to prevent bookings on Sundays and in the past.
- Track patient information, including names, ages, and genders.
- Easily extendable to include additional features or user roles.

## Installation

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/the-witty-one/doctors_appointment.git
   ```

2. Navigate to the project directory:

   ```bash
   cd appointment-management-system
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Initialize the SQLite database:

   ```bash
   python database.py
   ```

5. Run the FastAPI application:

   ```bash
   uvicorn main:app --host 0.0.0.0 --port 8000 --reload
   ```

The application should now be running and accessible at `http://localhost:8000`.

## Usage

### API Endpoints

- **Create a Doctor Profile**:

  ```http
  POST /doctor/
  ```

- **Retrieve a Doctor Profile by ID**:

  ```http
  GET /doctors/{doctor_id}/
  ```

- **Retrieve List of Doctors**:

  ```http
  GET /doctors/
  ```

- **Book an Appointment**:

  ```http
  POST /book-appointment/
  ```

- **Retrieve List of Patients**:

  ```http
  GET /patients/
  ```

### Sample Data

The application comes with sample data preloaded for testing purposes. You can remove the sample data and add your own doctors and patients through the API.

### Notes

- Appointments cannot be booked on Sundays.
- Past dates are not accepted for booking.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please follow the [Contributing Guidelines](CONTRIBUTING.md).
