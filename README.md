# Cloud RESTful API with Docker

## Overview
This project is a demonstration of my skills in **Python**, **RESTful API development**, and **Docker containerization**, with a focus on **cloud computing principles**. It was developed as part of an assignment for the **Cloud Computing and Software Engineering** course taught by Dr. Daniel Yellin. The main focus of the project is to create a **RESTful API** for managing meals and dishes, and to package and deploy the application using **Docker**.

## Main Focus
The main focus of the project is to:
- **Integrate with an external API** to retrieve and compute nutritional information for dishes.
- Use Docker to package the application, ensuring portability and ease of deployment.
- Integrate with an external API to compute nutritional information for dishes.
- Implement Docker Compose to manage multiple services, ensure persistence, and enable recovery from failures.

## Project Features

- **Retrieve, update, and delete dishes and meals**: Users can perform CRUD operations on dishes and meals.
- **Compute nutritional information**: When a dish is added, the application computes its calories, serving size, sodium, and sugar using the API Ninjas Nutrition API.
- **Uses Docker Compose**: Manages the application built from four services (meals service, diet service, database service, reverse-proxy service).
- **Ensures persistence**: Makes meals and diet services persistent.
- **Implements a reverse-proxy**: Uses NGINX to route requests to the appropriate server.
- **Handles failures**: Automatically restarts services after a failure and processes requests as if no failure occurred.
- **Load Balancing**: Implements load balancing for the meal service.

## API Endpoints

### Dishes
- `POST /dishes`: Add a new dish.
- `GET /dishes`: Retrieve all dishes.
- `GET /dishes/{ID or name}`: Retrieve a dish by ID or name.
- `DELETE /dishes/{ID or name}`: Delete a dish by ID or name.

### Meals
- `POST /meals`: Add a new meal.
- `GET /meals`: Retrieve all meals.
- `GET /meals/{ID or name}`: Retrieve a meal by ID or name.
- `DELETE /meals/{ID or name}`: Delete a meal by ID or name.
- `PUT /meals/{ID}`: Update a meal by ID.

### Diets
- `POST /diets`: Add a new diet.
- `GET /diets`: Retrieve all diets.
- `GET /diets/{name}`: Retrieve a diet by name.

## Docker Instructions

### Dockerfile
The `Dockerfile` is used to build a Docker image for the application. It includes all necessary dependencies and configurations to run the application.

### Docker Compose
The `docker-compose.yml` file defines the services, networks, and volumes for the application. It ensures that services are started in the correct order and can restart after failures.

## How to Run the Application

1. Clone the repository:
    ```sh
    git clone <repository_url>
    cd <repository_directory>
    ```

2. Build and run the Docker container:
    ```sh
    docker-compose up --build
    ```

## External API Integration
The application uses the [API Ninjas Nutrition API](https://api-ninjas.com/api/nutrition) to compute nutritional information for dishes.

## Testing
The application is tested by building the Docker image, running the container, and issuing REST requests to check the correctness of the responses.
