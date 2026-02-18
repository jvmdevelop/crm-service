<h1 align="center">crm-service</h1>
<p align="center" >
  <img alt="Java" src="https://img.shields.io/badge/Java-ED8B00?logo=openjdk&logoColor=white">
  <img alt="Spring Boot" src="https://img.shields.io/badge/Spring%20Boot-6DB33F?logo=spring-boot&logoColor=white">
  <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white">
  <img alt="React" src="https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=white">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white">
  <img alt="Status" src="https://img.shields.io/badge/status-beta-yellow">
  <img alt="License" src="https://img.shields.io/badge/license-ISC-blue">
</p>

<br>

**crm-service** is a comprehensive customer relationship management platform powered by Spring Boot and React, featuring project management, task tracking, team collaboration, and secure authentication.

## Features

- user authentication and authorization with JWT
- project and task management system
- team collaboration and member management
- real-time chat functionality
- password reset and email notifications
- postgresql database with JPA
- spring security integration
- restful API design
- react frontend with TypeScript
- ant design UI components
- docker compose support

## Installation

### Prerequisites:

- java 17 
- maven 3.6+
- postgresql database
- node.js 18+
- docker & docker compose 

### Backend Setup:

```bash
git clone git@github.com:jvmdevelop/crm-service.git
cd crm-service/backend
mvn clean install
mvn spring-boot:run
```

### Frontend Setup:

```bash
cd crm-service/frontend
npm install
npm run dev
```

### With Docker Compose:

```bash
cd crm-service
docker-compose up
```

## Usage

### Configuration

Configure your `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/crm_service
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

### Running the application:

**Backend:**
```bash
cd backend
mvn spring-boot:run
```

**Frontend:**
```bash
cd frontend
npm run dev
```

The application will be available at:
- Backend API: `http://localhost:8080`
- Frontend: `http://localhost:5173`

## API Endpoints

### Authentication

| Endpoint | Method | Description |
|:---------|:------:|:------------|
| `/api/auth/register` | POST | register new user |
| `/api/auth/login` | POST | user login |
| `/api/auth/me` | GET | get current user |
| `/api/auth/reset-password/initiate` | POST | initiate password reset |
| `/api/auth/reset-password` | POST | reset password |

### Project Management

| Endpoint | Method | Description |
|:---------|:------:|:------------|
| `/api/projects` | GET | get all projects |
| `/api/projects` | POST | create new project |
| `/api/projects/{id}` | PUT | update project |
| `/api/projects/{id}` | DELETE | delete project |

### Task Management

| Endpoint | Method | Description |
|:---------|:------:|:------------|
| `/api/tasks` | GET | get all tasks |
| `/api/tasks` | POST | create new task |
| `/api/tasks/{id}` | PUT | update task |
| `/api/tasks/{id}` | DELETE | delete task |

## Project Structure

- `backend/` - Spring Boot backend application
  - `src/main/java/com/mono/` - main package
  - `controllers/` - rest api controllers
  - `service/` - business logic services
  - `models/` - JPA entities
  - `repository/` - repository interfaces
  - `security/` - security configuration
  - `dto/` - data transfer objects
- `frontend/` - React frontend application
  - `src/` - source code
  - `src/components/` - React components
  - `src/pages/` - page components
  - `src/store/` - redux store

## Examples

Register a new user:

```bash
curl -X POST http://localhost:8080/api/auth/register \
  -H "Content-Type: application/json" \
  -d '{"username": "john_doe", "email": "john@example.com", "password": "securePassword"}'
```

Create a new project:

```bash
curl -X POST http://localhost:8080/api/projects \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -d '{"name": "New Project", "description": "Project description"}'
```

Create a new task:

```bash
curl -X POST http://localhost:8080/api/tasks \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_JWT_TOKEN" \
  -d '{"title": "Complete setup", "description": "Initial setup task", "projectId": 1}'
```

## Dependencies

### Backend:
- spring boot 3.3.4
- spring security
- spring data JPA
- spring mail
- postgresql driver
- JWT (jjwt)
- lombok
- SpringDoc OpenAPI
- swagger UI

### Frontend:
- react 18.3.1
- typescript
- ant design
- redux toolkit
- react router
- axios
- tailwind css
- vite

## Security Features

- jwt-based authentication
- password encryption
- role-based access control
- email verification
- password reset functionality
- cors configuration

## Contributing

1. fork the repository
2. create a feature branch
3. submit a pull request

## License

ISC license - see [LICENSE](LICENSE) for details.

## EOF
