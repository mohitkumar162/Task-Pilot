# TaskPilot

A production-ready role-based Task Management System built with **Spring Boot**, **Spring Security**, **PostgreSQL**, **JWT Authentication**, **Docker**, **GitHub Actions**, and **AWS EC2**.

TaskPilot enables managers to create projects, assign tasks, and monitor progress, while developers can securely update the status of their assigned tasks through JWT-protected REST APIs.

---

## Features

- JWT Authentication & Authorization
- Role-Based Access Control (Manager & Developer)
- Project & Task Management
- Task Status Tracking
- BCrypt Password Encryption
- RESTful APIs
- PostgreSQL Integration
- Docker & Docker Compose
- GitHub Actions CI/CD
- AWS EC2 Deployment
- Unit Testing with JUnit 5 & Mockito

---

## Tech Stack

| Category | Technology |
|----------|------------|
| Language | Java 17 |
| Framework | Spring Boot 3, Spring Security |
| Database | PostgreSQL |
| ORM | Spring Data JPA, Hibernate |
| Authentication | JWT, BCrypt |
| Frontend | HTML, CSS, JavaScript |
| Build Tool | Maven |
| Testing | JUnit 5, Mockito |
| DevOps | Docker, Docker Compose, GitHub Actions |
| Deployment | AWS EC2 |

---

## Architecture

```text
Browser
   │
   ▼
Frontend (HTML, CSS, JavaScript)
   │
REST API
   │
Spring Boot + Spring Security + JWT
   │
Service Layer
   │
Spring Data JPA
   │
PostgreSQL
```

---

## Project Structure

```text
Task-Pilot/
├── .github/workflows/ci.yml     # CI/CD pipeline
├── frontend/                    # Static HTML/CSS/JS client
├── taskmanagerbackend/
│   ├── src/main/java/com/taskmanager/
│   │   ├── config/              # Security & CORS config
│   │   ├── controller/          # REST controllers
│   │   ├── model/               # JPA entities
│   │   ├── repository/          # Spring Data repositories
│   │   ├── security/            # JWT filter & utils
│   │   └── service/             # Business logic
│   ├── src/test/java/           # Unit tests (Mockito)
│   └── Dockerfile
├── docker-compose.yml
├── screenshots/                 # Application screenshots
├── .env.example                 # Environment variable template
└── README.md
```

---

## Getting Started

Clone the repository:

```bash
git clone https://github.com/mohitkumar162/taskpilot-springboot.git
cd taskpilot-springboot
```

Create a `.env` file:

```env
DB_USERNAME=postgres
DB_PASSWORD=your_password

JWT_SECRET=your_secret_key
JWT_EXPIRATION_MS=86400000
SERVER_PORT=8080
```

Start the application:

```bash
docker compose up -d --build
```

The application will be available at:

```
http://localhost:8080
```

Run unit tests:

```bash
cd taskmanagerbackend
mvn clean verify
```

---

## CI/CD

The project uses **GitHub Actions** to:

- Run unit tests
- Build the Docker image
- Push the image to GitHub Container Registry
- Deploy the latest version to AWS EC2

---

## Deployment

The application is containerized using Docker and can be deployed on an AWS EC2 instance.

After deployment, access the application at:

```text
http://<EC2_PUBLIC_IP>:8080
```

---

## Security

- JWT Authentication
- Spring Security
- BCrypt Password Hashing
- Role-Based Authorization
- Stateless Session Management
- Environment-based Configuration

---

## Future Improvements

- Swagger/OpenAPI Documentation
- Refresh Token Authentication
- Dashboard Analytics
- Email Notifications
- File Attachments
- Task Comments
- Redis Caching
- Kubernetes Deployment

---

## Author

**Mohit Kumar**

- GitHub: https://github.com/mohitkumar162
- LinkedIn: https://www.linkedin.com/in/mohitkumar162/

---

## License

This project is licensed under the **MIT License**.
