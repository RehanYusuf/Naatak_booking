# 🎭 Rangmanch Reviews API

A RESTful API built with **FastAPI** for managing theatre reviews for Pune Rangmanch. The application provides an API backend with database table initialization and modular review routes.

## 🚀 Features

- **FastAPI Backend:** Built using FastAPI for a lightweight and high-performance API.
- **Database Initialization:** Automatically creates database tables when the application starts.
- **Modular Routing:** Review-related endpoints are organized using FastAPI routers.
- **Application Lifecycle Management:** Uses FastAPI's lifespan context manager for startup and shutdown events.
- **Root Endpoint:** Provides a welcome message to verify that the API is running.

## 🛠️ Tech Stack

- **Language:** Python
- **Backend Framework:** FastAPI
- **Server:** Uvicorn
- **Database:** Configured through the `data.py` module

## 📁 Project Structure

```text
rangmanch-reviews/
│
├── main.py
├── data.py
├── routes/
│   └── reviews.py
│
├── requirements.txt
└── README.md
```

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd rangmanch-reviews
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the virtual environment:

**Windows:**
```bash
venv\Scripts\activate
```

**Linux / macOS:**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install fastapi uvicorn
```

Install any additional dependencies required by your database and route modules.

Alternatively, if you have a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

### 4. Configure the Database

Ensure your database is configured correctly in `data.py` and that the required database server is running.

The application automatically initializes database tables during startup through the `create_tables()` function.

### 5. Run the Application

```bash
uvicorn main:app --reload
```

The API will be available at:

```text
http://127.0.0.1:8000
```

## 📖 API Documentation

FastAPI automatically generates interactive API documentation.

| Documentation | URL |
|---|---|
| Swagger UI | http://127.0.0.1:8000/docs |
| ReDoc | http://127.0.0.1:8000/redoc |

## 🔗 Available Endpoints

### Root Endpoint

**GET /**

Checks whether the application is running.

Example response:

```json
{
  "message": "Welcome to rangmanch reviews application"
}
```

### Reviews Endpoints

Review-related endpoints are registered through the router imported from:

```python
from routes.reviews import router as reviews_router
```

Refer to `routes/reviews.py` for the complete list of review endpoints.

## 🔄 Application Lifecycle

The application uses FastAPI's lifespan functionality:

- **Startup:** Calls `create_tables()` to initialize database tables.
- **Shutdown:** Prints a shutdown message.

## 🎯 Project Objective

Rangmanch Reviews API aims to provide a backend foundation for a theatre review platform focused on Pune Rangmanch, allowing review-related functionality to be organized and exposed through RESTful API endpoints.

## 👨‍💻 Author

**Yusuf Rehan**

---

⭐ If you find this project interesting, consider giving the repository a star!
