# Django-FastAPI-Nginx Project

This repository contains a Docker Compose setup for running a web application consisting of a Django app, a FastAPI app, and an Nginx reverse proxy. The Django app handles the main web interface, while the FastAPI app provides a RESTful API. Nginx acts as a reverse proxy, routing requests to the appropriate service based on the URL path.

## Prerequisites

- Docker
- Docker Compose

## File Structure
```
.
├── django_app
│   ├── Dockerfile
│   ├── manage.py
│   └── requirements.txt
├── fastapi_app
│   ├── Dockerfile
│   ├── main.py
│   └── requirements.txt
├── nginx
│   ├── Dockerfile
│   └── nginx.conf
└── docker-compose.yml
```
Copy code
- `django_app`: Contains the Django web application.
- `fastapi_app`: Contains the FastAPI API service.
- `nginx`: Contains the Nginx configuration files.
- `docker-compose.yml`: The Docker Compose file that defines the services and their configurations.

## Getting Started

1. Clone the repository:
git clone `https://github.com/vishwajeetvishwakarma/Route-Mapping-Nginx`
cd django-fastapi-nginx
Copy code
2. Build and start the containers:
docker-compose up --build
Copy code
This will build the Docker images and start the containers for the Django app, FastAPI app, and Nginx reverse proxy.

3. Access the application:

- The Django app will be available at `http://localhost/`
- The FastAPI app will be available at `http://localhost/api/`

Nginx will route requests to the appropriate service based on the URL path.

## Configuration

The Nginx configuration is defined in the `nginx/nginx.conf` file. This file contains the routing rules that determine which service should handle incoming requests based on the URL path.

The Docker Compose configuration is defined in the `docker-compose.yml` file. This file specifies the services, their configurations, and the networks used by the application.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
