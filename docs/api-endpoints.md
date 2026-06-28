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
