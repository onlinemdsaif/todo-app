# To-Do App

## Overview
This is a full-stack To-Do application with a frontend, backend, and a database. The application allows users to add, update, delete, and view their tasks.

## Features
- User authentication (if implemented)
- Add, update, delete, and list tasks
- Responsive frontend
- REST API backend
- Docker support (if applicable)

## Tech Stack
- **Frontend:** React.js (or any frontend framework used)
- **Backend:** Flask / Node.js
- **Database:** SQLite / PostgreSQL / MongoDB (whichever is used)
- **Docker:** Docker Compose (if used)

## Installation & Setup

### 1. Clone the Repository
```sh
git clone https://github.com/onlinemdsaif/todo-app.git
cd todo-app
```

### 2. Backend Setup
Navigate to the `backend` folder:
```sh
cd backend
```

- If using **Python (Flask)**:
  ```sh
  pip install -r requirements.txt
  flask run --host=0.0.0.0 --port=5000
  ```
- If using **Node.js (Express)**:
  ```sh
  npm install
  npm start
  ```

### 3. Frontend Setup
Navigate to the `frontend` folder:
```sh
cd ../frontend
```

- If using React:
  ```sh
  npm install
  npm start
  ```

### 4. Running with Docker (Optional)
If Docker Compose is used:
```sh
docker-compose up --build
```

## API Endpoints (Backend)
| Method | Endpoint      | Description           |
|--------|--------------|-----------------------|
| GET    | `/tasks`     | Fetch all tasks       |
| POST   | `/tasks`     | Add a new task        |
| PUT    | `/tasks/:id` | Update a task         |
| DELETE | `/tasks/:id` | Delete a task         |

## Troubleshooting
- If **backend is not running** on port `5000`:
  ```sh
  lsof -i :5000  # Check if port is in use
  kill -9 $(lsof -t -i :5000)  # Free the port
  ```
- If **frontend is not connecting to backend**, check `CORS` policy and backend URL in the frontend.
- If **Docker issues arise**, try rebuilding:
  ```sh
  docker-compose down && docker-compose up --build
  ```

## Contribution
Feel free to fork the repository and submit pull requests for improvements.

## License
This project is open-source and available under the MIT License.
