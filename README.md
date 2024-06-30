# Todo App with Django and DRF

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Running Tests](#running-tests)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This is a simple Todo application built with Django and Django REST Framework (DRF). The app allows users to create, read, update, and delete (CRUD) tasks through a RESTful API.

## Features

- User authentication and registration
- Create, read, update, and delete tasks
- Mark tasks as completed
- Filter tasks by status (completed or not completed)
- RESTful API with JSON responses

## Requirements

- Python 3.8+
- Django 3.2+
- Django REST Framework 3.12+

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/Todo-With-DRF.git
   cd todo-app-django-drf
   ```

2. **Create a virtual environment and activate it:**

   ```bash
   python -m venv env
   source env/bin/activate  # On Windows use `env\Scripts\activate`
   ```

3. **Install the required packages:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply the migrations:**

   ```bash
   python manage.py makemigraitons
   python manage.py migrate
   ```

5. **Create a superuser:**

   ```bash
   python manage.py createsuperuser
   ```

6. **Run the development server:**

   ```bash
   python manage.py runserver
   ```

7. **Access the app:**

   Open your browser and go to `http://127.0.0.1:8000/`

## Usage

- Use the Django admin panel to manage users and tasks at `http://127.0.0.1:8000/admin/`
- Use API endpoints to interact with tasks (see below).

## API Endpoints

| Method | Endpoint                | Description                  |
|--------|-------------------------|------------------------------|
| POST   | /api/register/          | Register a new user          |
| POST   | /api/login/             | Obtain authentication token  |
| GET    | /api/tasks/             | List all tasks               |
| POST   | /api/tasks/             | Create a new task            |
| GET    | /api/tasks/{id}/        | Retrieve a task by ID        |
| PUT    | /api/tasks/{id}/        | Update a task by ID          |
| DELETE | /api/tasks/{id}/        | Delete a task by ID          |

### Authentication

This app uses token-based authentication. Obtain a token by logging in, and include the token in the Authorization header for requests that require authentication.

```http
Authorization: Token your_token_here
```

## Running Tests

To run the tests, use the following command:

```bash
python manage.py test
```

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes. Make sure to update tests as appropriate.

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
