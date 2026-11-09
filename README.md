# RaceDay – Event Management System

## 1. Project Overview

RaceDay is an event management system developed using ASP.NET Core and C# with .NET 8.

The system allows organisers to create and manage running events, while participants can browse events, register for events, and view their results.

The application uses an ASP.NET Core MVC frontend that communicates with a RESTful Web API.

## 2. Technologies Used

- C#
- .NET 8
- ASP.NET Core MVC
- ASP.NET Core Web API
- SQL Server
- ADO.NET
- HTML5
- CSS3
- Bootstrap
- JavaScript
- Git and GitHub
- GitHub Actions

## 3. Main Features

### Participant Features

- Register an account.
- Log in and log out.
- Browse available events.
- View event details.
- Register for events.
- View personal enrolments.
- View event results.
- Manage profile information.

### Organiser Features

- Register as an organiser.
- Log in and log out.
- View organiser dashboard.
- Create events.
- Edit events.
- Delete events.
- Manage event categories.
- View participant enrolments.
- Capture participant results.

## 4. Project Structure

The solution contains the following main components:

- **RaceDay API** – Handles application data and business operations.
- **RaceDayWeb** – ASP.NET Core MVC frontend.
- **Models** – Application data models.
- **ViewModels** – Models used by MVC views.
- **Controllers** – Handle application requests.
- **Services** – Communicate with the RESTful API.
- **Views** – Razor pages displayed to users.
- **wwwroot** – CSS, JavaScript and static resources.

## 5. Requirements

Install the following software:

- Visual Studio 2022.
- .NET 8 SDK.
- SQL Server or SQL Server LocalDB.
- SQL Server Management Studio (SSMS).
- Git.

## 6. Database Setup

1. Open SQL Server Management Studio.
2. Connect to your SQL Server instance.
3. Create or restore the RaceDay database using the supplied database SQL script.
4. Check that the database connection string in the API project is correct.
5. Ensure the API can connect to the database.

## 7. Configuration

Configure the API URL in the RaceDayWeb `appsettings.json` file.

Example:

    {
      "ApiSettings": {
        "BaseUrl": "https://localhost:7100/"
      }
    }

Make sure this URL matches the API launch profile.

Do not commit passwords, database credentials, API keys or other secrets to GitHub.

## 8. Running the Application

### Step 1: Open the solution

Open the RaceDay solution in Visual Studio 2022.

### Step 2: Start the API

1. Set the RaceDay API project as the startup project.
2. Run the API.
3. Confirm that it starts successfully.

### Step 3: Start the MVC application

1. Set RaceDayWeb as the startup project.
2. Check the API BaseUrl in `appsettings.json`.
3. Run the MVC application.
4. Register or log in to use the application.

If the API and MVC projects are in the same solution, you can configure Visual Studio to start both projects together.

## 9. GitHub Setup

To upload the project to GitHub:

1. Create a new GitHub repository.
2. Make sure the repository does not contain old project history if you want a clean repository.
3. Open the project folder in a terminal.
4. Initialise Git and connect the new repository.

Example commands:

    git init
    git add .
    git commit -m "Initial RaceDay project"
    git branch -M main
    git remote add origin YOUR_NEW_GITHUB_REPOSITORY_URL
    git push -u origin main

Replace `YOUR_NEW_GITHUB_REPOSITORY_URL` with your actual repository URL.

## 10. Continuous Integration

This project uses GitHub Actions to automatically restore dependencies and build the .NET solution.

The workflow is located at:

    .github/workflows/dotnet.yml

The CI workflow runs when code is pushed to the main branch or when a pull request is created.

## 11. Security

- Passwords must be securely hashed.
- User roles control access to organiser and participant functionality.
- Organiser access must be checked by the API.
- Sensitive configuration values must not be committed to GitHub.
- Authentication and session information must be handled securely.

## 12. Author

RaceDay Event Management System

Developed as part of a .NET development project.
