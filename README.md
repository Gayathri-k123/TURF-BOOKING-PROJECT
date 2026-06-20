# Turf Booking Project

A multi-role web application for booking sports turfs online, built with Django. Supports three distinct user roles — platform Admin, per-turf Manager, and end Users — with live weather information integrated into the booking flow.

## Problem Statement
Booking a sports turf is typically a manual, phone-call-based process with no visibility into real-time availability. This project digitizes that process into a structured platform where turf owners can manage their listings and bookings, and users can browse, check conditions, and book a slot online.

## Features
- **Role-based access** across three apps:
  - **Admin** — manages the platform overall (turfs, users, bookings)
  - **Manager** — manages bookings and availability for their own assigned turf
  - **User** — browses available turfs, books a slot, and receives booking confirmation
- **Turf listings with images** (`media/turf_img`) for each venue
- **Live weather integration** — shows current weather for a turf's location, helping users make informed booking decisions for outdoor venues
- Booking confirmation flow for end users

## Tech Stack
- **Backend:** Python, Django
- **Database:** SQLite
- **Frontend:** HTML, CSS, SCSS, JavaScript
- **Third-party integration:** Weather API (via `weather_app`)

## Project Structure
```
TURF-BOOKING-PROJECT/
├── admin_app/         # Platform-wide administration (turfs, users, bookings)
├── manager_app/        # Per-turf manager dashboard and booking management
├── users_app/           # End-user browsing and booking flow
├── weather_app/          # Live weather lookup for turf locations
├── myworld/                # Django project settings/configuration
├── online_turf/              # Core Django app (project root config)
├── templates/                  # Shared HTML templates
├── static/                      # CSS, JS, and static assets
├── media/turf_img/                # Uploaded turf images
├── manage.py
└── README.md
```

## Installation
```bash
git clone https://github.com/Gayathri-k123/TURF-BOOKING-PROJECT.git
cd TURF-BOOKING-PROJECT
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```
Then open `http://127.0.0.1:8000` in your browser.

> Note: A weather API key is required for `weather_app` to function — see Configuration below.

## Configuration
This project uses a weather API to fetch live conditions for turf locations. You'll need to add your own API key (e.g. as an environment variable or in a local settings file not committed to GitHub) before running the weather feature.

## Usage
1. **As a User:** Browse available turfs, view live weather for the turf's location, select a slot, and confirm your booking.
2. **As a Manager:** Log in to view and manage bookings for your assigned turf.
3. **As an Admin:** Log in to manage turfs, users, and platform-wide bookings.

## Results
- A working three-tier role system (Admin/Manager/User) built on Django's authentication and app structure.
- Live weather data integrated directly into the user's booking decision flow.

## Future Improvements
- Add online payment integration for end-to-end booking
- Move from SQLite to a production-grade database (e.g. PostgreSQL) for deployment
- Add email/SMS booking confirmations
- Add `.gitignore` and remove the committed `db.sqlite3` from version control
- Add automated tests for booking logic (e.g. preventing double-booking of the same slot)
- Deploy to a live hosting platform with a public demo link

## Author
Gayathri K — MCA Graduate | [LinkedIn](https://www.linkedin.com/in/gayathri-k-62427a2b3) | [GitHub](https://github.com/Gayathri-k123)
