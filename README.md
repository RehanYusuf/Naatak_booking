🎭 Rangmanch Reviews APIA fast, lightweight RESTful backend API built with FastAPI for managing and exploring theatre reviews for Pune Rangmanch.✨ FeaturesFastAPI Framework: High-performance asynchronous Python web framework with automatic interactive API documentation.Automated Database Setup: Uses FastAPI's lifespan context manager to automatically initialize database tables on startup.Modular Routing: Clean separation of concerns with dedicated route modules (routes/reviews.py) and database layer (data.py).Interactive API Docs: Built-in Swagger UI and ReDoc support out of the box.📁 Project Structurerangmanch-reviews-api/
├── main.py              # Application entry point, FastAPI setup & lifespan events
├── data.py              # Database connection & table creation logic
├── routes/
│   └── reviews.py       # API endpoints for theatre reviews
├── requirements.txt     # Project dependencies
└── README.md            # Project documentation
🛠️ Tech StackLanguage: Python 3.10+Framework: FastAPIASGI Server: Uvicorn🚀 Getting Started1. Clone the Repositorygit clone https://github.com/<your-username>/rangmanch-reviews-api.git
cd rangmanch-reviews-api
2. Create and Activate a Virtual EnvironmentWindows (PowerShell):python -m venv venv
.\venv\Scripts\Activate.ps1
macOS / Linux:python3 -m venv venv
source venv/bin/activate
3. Install Dependenciespip install fastapi uvicorn
(Or if you have a requirements.txt file: pip install -r requirements.txt)4. Run the Applicationuvicorn main:app --reload
On startup, the application will automatically initialize the database tables and start the development server at http://127.0.0.1:8000.
📖 API DocumentationOnce the server is running, you can explore and test all endpoints interactively:Swagger UI: http://127.0.0.1:8000/docsReDoc: http://127.0.0.1:8000/redocBase EndpointMethodEndpointDescriptionGET/Health check / Welcome message ("Welcome to rangmanch reviews application")*/reviews (see /docs)Theatre review endpoints mounted via reviews_router🤝 ContributingFork the repository.Create a new feature branch (git checkout -b feature/your-feature).Commit your changes (git commit -m "Add your feature").Push to the branch (git push origin feature/your-feature).Open a Pull Request.
