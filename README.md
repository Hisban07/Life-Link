# LifeLink 2.0

LifeLink 2.0 is a blood donation and hospital coordination platform designed to help patients quickly find compatible donors, while allowing hospitals and administrators to manage donation requests and donor eligibility efficiently.

The project combines a modern React frontend with a secure ASP.NET Core backend and SQL Server database to provide a complete donor-matching experience.

## Overview

This application supports:

- Donor registration and profile management
- Blood group compatibility checking
- Donor eligibility validation based on the 90-day donation rule
- Hospital request tracking and blood availability management
- Patient and hospital blood request workflows
- JWT-based authentication and authorization
- Admin dashboard for operational oversight
- Review and trust-building feedback from users

## Tech Stack

Frontend
- React
- Vite
- JavaScript
- Framer Motion
- Recharts
- Lucide React
- Axios

Backend
- ASP.NET Core Web API
- C#
- Entity Framework Core
- SQL Server
- JWT Authentication
- Swagger/OpenAPI

## Project Structure

```text
Life-Link/
├── backend/
│   ├── Controllers/
│   ├── Data/
│   ├── DTOs/
│   ├── Helpers/
│   ├── Interfaces/
│   ├── Models/
│   ├── Properties/
│   ├── Repositories/
│   ├── Services/
│   ├── appsettings.json
│   ├── appsettings.Development.json
│   ├── LifeLink.API.csproj
│   ├── LifeLinkDB_Setup.sql
│   ├── Program.cs
│   └── README-DATABASE.md
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   ├── vite.config.js
│   └── index.html
├── oop_csharp_report.md
├── README.md
└── .gitignore
```

## Main Features

### 1. Smart Donor Matching
The app evaluates blood compatibility and donor availability using logical matching rules to help connect patients with suitable donors quickly.

### 2. 90-Day Eligibility Rule
Donors are marked as eligible or waiting depending on how long it has been since their last donation.

### 3. Hospital Network
Hospitals can manage their blood availability, request blood, and track pending requests.

### 4. Authentication and Authorization
Users can register and sign in using email/password authentication secured with JWT tokens.

### 5. Admin Controls
Admins can view and manage the system more broadly, including donor and request-related workflows.

### 6. Community Trust
The app includes user reviews and testimonials to build confidence and awareness.

## Database

The project uses SQL Server as its primary database and includes a setup script:

- `backend/LifeLinkDB_Setup.sql`
- `backend/README-DATABASE.md`

The application is configured through the connection string in:

- `backend/appsettings.json`

Example connection string:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=DESKTOP-DKRQJVF\\SQLEXPRESS;Database=LifeLinkDB;Trusted_Connection=True;TrustServerCertificate=True;"
}
```

## Authentication

The backend uses JWT authentication with a configured issuer, audience, and secret key in `backend/appsettings.json`.

Demo admin credentials seen in the frontend:

- Email: `admin@lifelink.com`
- Password: `admin123`

## Prerequisites

Before running the app, make sure you have:

- .NET SDK 10.0+
- SQL Server instance running locally or remotely
- Node.js and npm
- A modern browser

## Running the Backend

From the repository root:

```bash
cd backend

dotnet restore
dotnet run
```

The API will run using the configured ASP.NET Core app and automatically apply database initialization logic if the database is available.

## Running the Frontend

From the repository root:

```bash
cd frontend

npm install
npm run dev
```

This starts the Vite development server.

## Default Frontend URL

The app is configured to allow frontend connections through local development ports such as:

- `http://localhost:5173`
- `http://localhost:3000`

## API Documentation

Swagger is enabled in development mode, which allows you to explore and test endpoints via:

- `https://localhost:5000/swagger` or the local port used by the ASP.NET server

## Environment Notes

- The project is designed for local development and testing.
- Database credentials and server names should be updated to match your local environment.
- For production, secure the JWT secret and database connection details using environment variables or a secure configuration system.

## Screens & User Experience

The frontend includes pages for:

- Home
- Authentication
- Donor directory
- Find blood donor
- Hospitals
- Reviews
- Admin dashboard

These pages use animated UI patterns and a clean medical-themed design focused on trust, speed, and donation awareness.

## Contribution

Contributions are welcome. To contribute:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request with a clear summary

## License

This project does not currently include a repository license file. Please check with the repository owner for licensing details before commercial use or redistribution.

## Summary

LifeLink 2.0 is a practical healthcare-tech project that brings together blood donation coordination, donor verification, and hospital management in one application. It is especially useful for organizations or communities that need a fast, transparent, and digital approach to blood donation matching.

