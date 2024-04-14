# Game Store API

## Overview

Welcome to the Game Store API project! This project serves as the backend for a game store application, providing endpoints to manage games and genres. It is built using C# ASP.NET and Entity Framework.

## Entities

### Genre

- **Properties**:
  - `Id`: An integer representing the unique identifier for the genre.
  - `Name`: A string representing the name of the genre.

### Game

- **Properties**:
  - `Id`: An integer representing the unique identifier for the game.
  - `Name`: A string representing the name of the game.
  - `GenreId`: An integer representing the foreign key referencing the genre of the game.
  - `Genre`: A navigation property representing the genre of the game.
  - `Price`: A decimal representing the price of the game.
  - `ReleaseDate`: A `DateOnly` object representing the release date of the game.

## Installation

1. Clone this repository to your local machine.
2. Open the solution file (`GameStore.sln`) in Visual Studio.
3. Build the solution to restore dependencies.
4. Set up your database connection string in `appsettings.json`.
5. Run Entity Framework migrations to create the database schema:
   ```
   dotnet ef database update
   ```
6. Start the application.

## Usage

- Use API endpoints to perform CRUD operations on games and genres.
- Endpoint examples:
  - `GET /api/genres`: Retrieve all genres.
  - `GET /api/games`: Retrieve all games.
  - `POST /api/games`: Create a new game.
  - `PUT /api/games/{id}`: Update an existing game.
  - `DELETE /api/games/{id}`: Delete a game by ID.

## Contributing

Contributions are welcome! If you find any bugs or have suggestions for improvements, please feel free to open an issue or submit a pull request.
