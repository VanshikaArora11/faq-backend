# FAQ Project Documentation
# Django FAQ API with Multilingual Support

## Overview
This project is a Django-based API for managing FAQs with multilingual support. It allows users to create FAQs with automatic translations using Google Translate and supports a WYSIWYG editor for formatting answers. It also implements caching using Redis for optimized performance.

## Features
Multilingual FAQs (English, Hindi, Bengali) 
 WYSIWYG Editor (django-ckeditor) 
 REST API with Django Rest Framework 
 Automatic Translation via Google Translate API 
 Redis-based Caching for Faster Performance 
 Django Admin Panel for FAQ Management 
 Docker Support for Easy Deployment 
 Unit Tests using pytest 
 PEP8 Compliance & Git Best Practices 

## Installation

### 1. Clone the Repository
```sh
git clone <repository-url>
cd faq_project
```

### 2. Create & Activate Virtual Environment
```sh
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### 3. Install Dependencies
```sh
pip install -r requirements.txt
```

### 4. Apply Migrations
```sh
python manage.py migrate
```

### 5. Run the Server
```sh
python manage.py runserver
```

## Project Structure
```
faq_project/
│── faq_app/
│   ├── models.py   # FAQ Model
│   ├── views.py    # API Views
│   ├── urls.py     # API Routes
│   ├── serializers.py  # DRF Serializers
│   ├── admin.py    # Admin Panel Integration
│── settings.py     # Django Settings
│── urls.py         # Project URL Configuration
│── requirements.txt # Dependencies
│── Dockerfile      # Docker Configuration
│── docker-compose.yml # Docker Compose Configuration
│── manage.py       # Django CLI Tool
```

## API Endpoints

### 1. Fetch All FAQs (Default: English)
```sh
GET /api/faqs/
```

### 2. Fetch FAQs in Hindi
```sh
GET /api/faqs/?lang=hi
```

### 3. Fetch FAQs in Bengali
```sh
GET /api/faqs/?lang=bn
```

### 4. Create a New FAQ
```sh
POST /api/faqs/
Content-Type: application/json
{
  "question": "What is Django?",
  "answer": "Django is a high-level Python web framework."
}
```

## Running Tests
```sh
pytest
```

## Docker Support
### 1. Build & Run the Docker Container
```sh
docker-compose up --build
```

## Deployment
To deploy on Heroku or AWS, configure environment variables and use:
```sh
gunicorn faq_project.wsgi:application --bind 0.0.0.0:8000
```

## Git Best Practices
```sh
git commit -m "feat: Add multilingual FAQ model"
git commit -m "fix: Improve translation caching"
git commit -m "docs: Update README with API examples"
```

## Contribution Guidelines
1. Fork the repository.
2. Create a new branch (`feature-branch`).
3. Commit changes following conventional commit messages.
4. Submit a pull request for review.

This documentation ensures you can  easily install, run, and contribute  to the project! 🚀
