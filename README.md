# GoWheels

A full-stack vehicle marketplace platform built with ASP.NET Core (.NET 8), PostgreSQL, MongoDB, and Docker. GoWheels enables users to browse, post, and review vehicle listings, with an AI assistant providing summaries and sentiment analysis.

## Tech Stack

-   **Backend**: ASP.NET Core 8
-   **Databases**: PostgreSQL 15, MongoDB 7
-   **Containerization**: Docker
-   **AI**: OpenRouter API

## Installation

1.  **Ensure Docker and Docker Compose are installed.**
2.  **Create environment files:**
    *   Copy `.env.example` to `.env`.
    *   Add your `OPENROUTER_API_KEY` to the `.env` file.
    ```bash
    # Copy the example environment file
    cp .env.example .env

    # Open .env file in your editor and add your API key
    # Example:
    # OPENROUTER_API_KEY=your_api_key_here
    ```
3.  **Launch the supporting services (Databases):**
    ```bash
    docker compose up -d
    ```
4.  **Run the application using the .NET CLI:**
    ```bash
    # Navigate to the project directory (if not already there)
    # cd path/to/your/project

    # Restore dependencies
    dotnet restore GoWheels/GoWheels.csproj

    # Run the application
    dotnet run --project GoWheels/GoWheels.csproj
    ```
5.  **Access the application in your browser:**
    ```
    http://localhost:5237
    ```

### Default Accounts

| Role   | Email                     | Password     |
| ------ | ------------------------- | ------------ |
| Admin  | `admin@gowheels.local`    | `Password123!` |
| Expert | `expert@gowheels.local`   | `Password123!` |
| User   | `user@gowheels.local`     | `Password123!` |

## Management

```bash
# Stop the supporting services (Databases)
docker compose down
# Stop the supporting services and drop data volumes (Databases)
docker compose down -v
```
