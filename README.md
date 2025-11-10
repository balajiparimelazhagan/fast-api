# Fast API

FastAPI-based boilerplate API.

## Setup

### Prerequisites

- Python 3.11+
- Docker and Docker Compose
- PostgreSQL (via Docker)

### Installation

1. Clone the repository
2. Copy `.env.example` to `.env` and configure your environment variables:
   ```bash
   cp .env.example .env
   ```

3. Start the application using Docker Compose:
   ```bash
   docker-compose up --build
   ```

The API will be available at `http://localhost:8000`

### Environment Variables

- `DATABASE_URL`: PostgreSQL connection string
- `CORS_ORIGINS`: Comma-separated list of allowed CORS origins

See `.env.example` for default values.

## API Documentation

Once the application is running, you can access:

- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

## Development

### Running Locally

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Set up environment variables in `.env`

3. Run the application:
   ```bash
   uvicorn app.main:app --reload
   ```

## Project Structure

```
app/
├── __init__.py
├── main.py          # FastAPI application
├── config.py        # Configuration settings
├── db.py            # Database connection
├── exceptions.py    # Custom exceptions
├── models/          # SQLAlchemy models
├── routes/          # API routes
└── services/        # Business logic
```

## Health Check

Check API health:
```bash
curl http://localhost:8000/health
```
