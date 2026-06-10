# GoWheels

A full-stack vehicle marketplace platform built with ASP.NET Core (.NET 8), PostgreSQL, MongoDB, and Docker. GoWheels enables users to browse, post, and review vehicle listings, with an AI assistant providing summaries and sentiment analysis.

## Tech Stack

-   **Backend**: ASP.NET Core 8
-   **Databases**: PostgreSQL 15, MongoDB 7
-   **Containerization**: Docker
-   **AI**: OpenRouter API

## Installation

```bash
# Ensure Docker and Docker Compose are installed
docker --version
docker compose version

# Download the Docker Compose file
curl -O https://raw.githubusercontent.com/AmrDroid-git/GoWheelsWebsite/master/docker-compose.yml

# Launch the application (replace 'your_api_key_here' with your OpenRouter API key)
OPENROUTER_API_KEY=your_api_key_here docker compose -f docker-compose.yml up -d

# Access the application in your browser
echo "http://localhost:8080"
```

### Default Accounts

| Role   | Email                     | Password     |
| ------ | ------------------------- | ------------ |
| Admin  | `admin@gowheels.local`    | `Password123!` |
| Expert | `expert@gowheels.local`   | `Password123!` |
| User   | `user@gowheels.local`     | `Password123!` |

## Management

```bash
# Stop the application
docker compose down

# Full cleanup (stops containers and removes database data volumes)
docker compose down -v

# View application logs
docker logs gowheels_app
```