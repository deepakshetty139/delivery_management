Delivery Management System
A full-stack web application to manage vehicle services and components for a delivery management system. This system allows users to register components, manage vehicle repairs, log issues, calculate final prices, and simulate payment processing. A responsive dashboard with graphs for revenue statistics is also included.

Project Overview
This project is built to manage vehicle services and track related transactions within a delivery management system. It consists of:
- backend server created with Django to manage APIs and data storage.
- frontend application built with React to provide an interactive user interface.

Tech Stack
Backend: Django, Django REST Framework
Frontend: React, Axios, Recharts
Database: SQLite (default, can be changed in settings.py)
Other Libraries: Jest (for frontend testing), React Testing Library

Features
-Component Management: Register components with repair or purchase pricing.
-Vehicle Management: Add and manage repair vehicles.
-Issue Tracking: Track vehicle issues, including component repair or purchase.
-Final Price Calculation: Calculate and simulate payments (no real-world transactions).
-Revenue Charts: View daily, monthly, and yearly revenue with responsive graphs (using Recharts).
-Unit Tests: Basic unit tests for both backend and frontend.

Setup Instructions
Prerequisites
-Node.js (v16.x is recommended for compatibility)
-Python (v3.6+)
-npm (Node package manager)

Backend Setup (Django)
1.Navigate to the backend directory:
-cd delivery_management

2.Create a virtual environment (recommended):
-python -m venv venv
-source venv/bin/activate 

3.nstall backend dependencies:
-pip install -r requirements.txt

4.Configure and Run Migrations:
-python manage.py makemigrations
-python manage.py migrate

5.Create a superuser (for Django admin access):
-python manage.py createsuperuser

6.Start the Django server:
-python manage.py runserver

By default, Django runs on http://localhost:8000

Frontend Setup (React)
1.Navigate to the frontend directory:
-cd frontend

2.Install frontend dependencies:
-npm install

3.Configure Axios:
In src/services, ensure API_URL is set to http://localhost:8000 to match the Django server URL.

4.Start the React development server:
-npm start

By default, React runs on http://localhost:3000.

Note: If you encounter issues with npm start, set the env

ironment variable NODE_OPTIONS=--openssl-legacy-provider before running the start command.

Running the Application
1.Backend: Ensure Django server is running on http://localhost:8000:
-python manage.py runserver

2.Frontend: Ensure React server is running on http://localhost:3000:
npm start

Once both servers are running, visit http://localhost:3000 to access the Delivery Management System interface.

Testing
Django Unit Tests (Backend)

1.Navigate to the Django project directory:
-cd delivery_management

2.Run the tests:
-python manage.py test

Jest Tests (Frontend)
1.Navigate to the frontend directory:
-cd frontend

2.Run Jest tests:
-npm test

Project Structure
delivery_management/
├── frontend/                     # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/           # Reusable components
│   │   ├── pages/                # Pages for different features
│   │   ├── services/             # Axios services for API calls
│   │   └── App.js                # Main React app
│   └── package.json              # Frontend dependencies
├── vehicle_service/              # Django app for vehicle services
│   ├── migrations/
│   ├── models.py                 # Django models
│   ├── serializers.py            # Django serializers
│   ├── tests.py                  # Django tests
│   └── views.py                  # Django views (API)
├── delivery_management/          # Django project settings
│   ├── settings.py
│   └── urls.py
├── manage.py                     # Django CLI utility
└── README.md                     # Project documentation




