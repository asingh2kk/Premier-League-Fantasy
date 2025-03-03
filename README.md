## Project Overview

This is a backend project that consists of a simple CRUD application, designed to allow users to search for players in the Fantasy Premier League. 
The application includes a REST API that interacts with a PostgreSQL database, allowing users to query and retrieve player data based on specific criteria (team, position, nationality, etc.).

---

## Features

- **Search for players**: Users can filter players by team, position, or nationality.
- **Add, update, and delete players**: Full CRUD functionality for managing players.
- **Spring Boot Backend**: Utilizes Spring Boot for creating the REST API.
- **PostgreSQL Database**: Data is stored in a PostgreSQL database, with data from a CSV file being migrated into the database.
- **Data Scraping**: The project includes a data scraper that periodically scrapes the latest player data, ensuring that the database is always up to date with the most current player information.

---

## Technologies Used

- **Java**: The language used for backend development.
- **Spring Boot**: Framework used for building the backend REST API.
- **PostgreSQL**: The database management system used to store player data.
- **Maven**: A build automation tool used for project management and dependencies.

---

## Setup and Installation

Follow these steps to set up the project on your local machine:

### 1. Install Prerequisites

Make sure you have the following tools installed on your machine:

- **Java 23**
- **PostgreSQL**
- **IntelliJ IDEA** (or any IDE of your choice)

### 2. Clone the Repository

Clone the project from GitHub:

```bash
git clone <repo_url>
```

### 3. Set Up PostgreSQL Database

1. Create a database in PostgreSQL.
2. Grant all privileges to the user you’ll be using for the connection.
3. Import the player data CSV file into the PostgreSQL database.

### 4. Configure Database Connection

Modify the `application.properties` file under `src/main/resources/` to set up the database connection details.

---

## Running the Application

To run the application, follow these steps:

1. Open the project in IntelliJ IDEA or your preferred IDE.
2. Make sure the Java version is set to Java 23.
3. Run the application using the following command:

```bash
./mvnw spring-boot:run
```

4. Once the application starts, open your browser and navigate to `http://localhost:8080`. You should see the API running.

---

## Endpoints

### GET /api/v1/players

- **Description**: Fetch all players.
- **Query Parameters**:
  - `team`: Filter by team name.
  - `position`: Filter by player position.
  - `nation`: Filter by player's nationality.

### GET /api/v1/player/{name}

- **Description**: Fetch a player by their name.

### POST /api/v1/player

- **Description**: Add a new player.
- **Request Body**: JSON representation of a player.

### PUT /api/v1/player/{name}

- **Description**: Update an existing player by name.
- **Request Body**: JSON representation of the player to be updated.

### DELETE /api/v1/player/{name}

- **Description**: Delete a player by name.

---

## Hosting

For hosting the database and backend, you can use:

- **Supabase** for PostgreSQL database hosting.
- **Heroku** for backend deployment.
