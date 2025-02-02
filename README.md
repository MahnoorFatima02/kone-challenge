# SeaShell API

SeaShell API is a Flask-based web application for managing sea shells. It provides a RESTful API for creating, reading, updating, and deleting shell records.

## Table of Contents

- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Running the Application](#running-the-application)
- [Running Tests](#running-tests)
- [API Documentation](#api-documentation)
- [Database Migrations](#database-migrations)
- [Docker Setup](#docker-setup)

## Prerequisites

- Python 3.8+
- Flask==2.0.1
- Flask-SQLAlchemy==2.5.1
- Flask-Migrate
- Flask-Cors==3.0.10
- Flask-Swagger-UI==3.36.0
- Pytest==6.2.4
- Pytest-asyncio==0.15.1
- Docker

## Testing

- unittest.mock (included in Python standard library)
- MagicMock (part of unittest.mock)

## Setup 

**Clone the repository**:

   ```sh
   git clone https://github.com/yourusername/SeaShellProject.git

   cd SeaShellProject/backend
   ```

**Create a virtual environment**:

```sh
python3 -m venv venv
source venv/bin/activate
```

**Install dependencies**:

```sh  
pip install -r requirements.txt
``` 

**Set up environment variables**:

Create a .env file in the backend directory and add the following environment variables:
```sh 
SECRET_KEY = 'your-secret-key-here'
   ```


 ## Running application backend

```sh
cd SeaShellProject/backend
flask run
```
## Running the application frontend

```sh
cd ../frontend
npm install
npm start   
```

 ## Running tests

```sh
cd SeaShellProject/backend
pytest tests/seashell_api_tests.py
```

## API Documentation
The API documentation is available at http://localhost:5000/api/docs.

## Database Migrations
Database migrations are managed using Flask-Migrate. To create a new migration, run:
```sh
flask db migrate -m "Description of the migration"
```
## Docker Setup
To set up the MySQL database using Docker Compose, follow these steps:

1. Navigate to the Docker directory:
   ```sh
   cd docker 
   ```
2. Start the Docker containers:
```sh
docker-compose up -d
```
## Additional Information
**Swagger UI**: The Swagger UI for API documentation is available at http://localhost:5000/api/docs.
**Database**: The application uses MySQL as the database. The database configuration is specified in the docker-compose.yml file and the .env file.


