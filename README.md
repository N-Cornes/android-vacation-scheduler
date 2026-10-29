# Android Vacation Scheduler

A native Android application designed and developed by Nicholas Cornes for organizing vacations and related excursions with local persistent storage, date validation, alerts, and sharing features.

## Tech Stack

- Java
- Android SDK
- Android Studio
- Room Persistence Library
- SQLite
- XML Layouts

## Core Features

- Create, view, edit, and delete vacations
- Create, view, edit, and delete excursions
- Associate multiple excursions with a vacation
- Prevent deletion of vacations that still contain excursions
- Strict `MM/dd/yyyy` date validation
- Validate vacation end dates occur after start dates
- Validate excursion dates fall within the associated vacation dates
- Set alerts for vacation start and end dates
- Share vacation details using Android sharing functionality
- Persist data locally with Room and SQLite
- View excursions for an individual vacation
- View all stored excursions

## Data Model

The application uses two primary entities:

- **Vacation** — stores vacation title, hotel, start date, and end date
- **Excursion** — stores excursion details and maintains a relationship with a vacation

Room provides the persistence layer and DAO interfaces handle database operations.

## Application Structure

```text
Android Activities / XML Layouts
            ↓
        DAO Layer
            ↓
          Room
            ↓
         SQLite
```

Separate activities are used for vacation lists, vacation details, excursion lists, and excursion details.

## Validation

The application includes validation for important scheduling rules, including:

- Required date format
- Vacation end date after start date
- Excursion date within vacation date range
- Relationship protection when deleting vacations

These checks help prevent inconsistent scheduling data from being stored.

## Android Features

The application uses Android platform functionality for:

- Scheduled notifications and alerts
- Sharing vacation information
- Activity-based navigation
- Persistent local application data

## What I Built

I developed the application as a multi-screen Android scheduling system and implemented the Room database layer, vacation/excursion relationships, CRUD workflows, date validation, alerts, sharing, and relationship constraints.

## Source Code

The complete implementation is maintained in a private repository. Source access can be provided for professional review upon request.

## Author

**Nicholas Cornes**  
B.S. Software Engineering
