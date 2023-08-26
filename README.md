# Hospital COVID-19 Management API

This project aims to provide an API for doctors in a government-designated hospital to manage the testing, quarantine, and well-being of COVID-19 patients. The API allows two types of users: doctors and patients.

## Features

- Doctors can log in to the system.
- Doctors can register patients using their phone numbers. If the patient already exists, their information is returned.
- After patient checkup, doctors can create patient reports including status, date, and additional information.
- Patient reports include:
  - Created by doctor
  - Status (Negative, Travelled-Quarantine, Symptoms-Quarantine, Positive-Admit)
  - Date

## User Types

1. **Doctors**: Medical professionals responsible for patient care.
   - Routes:
     - `/doctors/register`: Register with username and password.
     - `/doctors/login`: Obtain a JWT token for authentication.

2. **Patients**: Individuals undergoing COVID-19 testing and quarantine.
   - Routes:
     - `/patients/register`: Register as a patient.
     - `/patients/:id/create_report`: Create a patient report.
     - `/patients/:id/all_reports`: List all reports of a patient, ordered from oldest to latest.

3. **Reports**:
   - `/reports/:status`: List all reports of all patients filtered by a specific status.

## Authentication

Certain routes require authentication using JWT tokens.

## Setup and Installation

1. Clone the repository: `git clone https://github.com/AnkitSingh2129/Hospital-Api`
2. Navigate to the project directory: `cd Hospital-Api`
3. Install dependencies: `npm install`
4. Run the server: `npm start`

## Contributing

We welcome contributions from the community! To contribute:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make changes and commit: `git commit -am 'Add new feature'`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Create a pull request.


