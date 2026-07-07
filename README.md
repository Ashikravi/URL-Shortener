# URL Shortener Service

A Django-based URL shortening service with unique code generation, duplicate detection, and click analytics — containerized with Docker for consistent deployment.

## Features

- **Short link generation** — converts long URLs into unique, shareable short codes
- **Validation & duplicate detection** — checks incoming URLs and prevents duplicate entries from generating redundant short codes
- **Analytics dashboard** — tracks clicks per short link and displays usage stats
- **Containerized** — fully set up with Docker and Docker Compose for isolated, reproducible environments

## Tech Stack

- **Backend:** Python, Django
- **Database:** MySQL
- **Deployment:** Docker, Docker Compose

## Quick Start

You can run this project either with Docker (recommended) or manually.

### Option 1: Docker Setup (Recommended)

**Prerequisites**
- Docker Desktop installed and running

**Build and run:**
```bash
docker compose up --build
```

The server starts inside the container at `http://0.0.0.0:8000/`. Once it's up, your app is available at `http://localhost:8000/`.

**Other useful commands:**
```bash
docker compose down      # stop the application
docker compose logs      # view logs
```

> If you hit errors with the Docker image, fall back to the manual setup below.

### Option 2: Manual Setup (No Docker)

**Prerequisites**
- Python 3.8+
- pip

**Steps:**
```bash
# 1. Clone the repository
git clone <your-repo-url>
cd <project-name>

# 2. Create a virtual environment
python -m venv myenv

# 3. Activate it
source myenv/bin/activate      # macOS/Linux
myenv\Scripts\activate         # Windows

# 4. Install dependencies
pip install -r requirements.txt

# 5. Run migrations
python manage.py migrate

# 6. Start the server
python manage.py runserver
```

Then open `http://127.0.0.1:8000` in your browser.

To exit the virtual environment when done:
```bash
deactivate
```
