# Campus Navigating System Application

A **Java Swing GUI** application to interact with a MySQL database named `campus1`. It allows users to perform **CRUD (Create, Read, Update, Delete)** operations on multiple campus-related tables like **Buildings, Departments, Facilities, POIs, Paths, Users, and Events**.

---

## 🚀 Features

- **Table Selection**: Choose any table using a dropdown menu.
- **Dynamic Form Fields**: Automatically generated fields based on the selected table.
- **Add Records**: Insert new data.
- **Update Records**: Modify existing data using the primary key.
- **Delete Records**: Remove data using the primary key.
- **View Records**: Retrieve and display a record by its primary key.

---

## 🛠️ Prerequisites

- **Java Development Kit (JDK 8 or above)**
- **MySQL Server** (running locally or remotely)
- **MySQL JDBC Driver** (`mysql-connector-java-x.x.x.jar`)

---

## 🗃️ Database Schema

### `campus1` database with the following tables:

#### Buildings
- `BuildingID` (INT, PK)
- `Name` (VARCHAR)
- `LocationLat` (FLOAT)
- `LocationLong` (FLOAT)
- `Address` (VARCHAR)
- `Floors` (INT)

#### Departments
- `DepartmentID` (INT, PK)
- `Name` (VARCHAR)
- `BuildingID` (INT, FK)
- `ContactInfo` (VARCHAR)
- `Head` (VARCHAR)

#### Facilities
- `FacilityID` (INT, PK)
- `Name` (VARCHAR)
- `LocationLat` (FLOAT)
- `LocationLong` (FLOAT)
- `Description` (VARCHAR)
- `Type` (VARCHAR)

#### POIs
- `POIID` (INT, PK)
- `Name` (VARCHAR)
- `LocationLat` (FLOAT)
- `LocationLong` (FLOAT)
- `Description` (VARCHAR)

#### Paths
- `PathID` (INT, PK)
- `StartLocationLat` (FLOAT)
- `StartLocationLong` (FLOAT)
- `EndLocationLat` (FLOAT)
- `EndLocationLong` (FLOAT)
- `Distance` (FLOAT)
- `Time` (INT)
- `Description` (VARCHAR)

#### Users
- `UserID` (INT, PK)
- `Name` (VARCHAR)
- `Email` (VARCHAR)
- `Role` (VARCHAR)
- `LastKnownLocationLat` (FLOAT)
- `LastKnownLocationLong` (FLOAT)

#### Events
- `EventID` (INT, PK)
- `Title` (VARCHAR)
- `Description` (VARCHAR)
- `Location` (VARCHAR)
- `EventDate` (DATE)
- `EventTime` (TIME)
- `Organizer` (VARCHAR)

---

## ⚙️ Setup Instructions

### 1. Download JDBC Driver
- Visit: https://dev.mysql.com/downloads/connector/j/
- Download the **platform-independent** `.jar` file
- Place it in a `lib/` directory within your project

### 2. Configure Database Credentials
Edit the following variables in `CampusNavigatingSystemApp.java`:

```java
private static final String DB_URL = "jdbc:mysql://localhost:3306/campus1";
private static final String USER = "root";
private static final String PASS = "Soumya@1411";

CampusNavigatingSystem/
├── lib/
│   └── mysql-connector-java-x.x.x.jar
├── src/
│   ├── CampusNavigatingSystemApp.java
│   └── Test.java
└── README.md
