# 📦 Amazon Price Tracker (Full Docker Setup)
This repository contains the complete Dockerized Amazon Price Tracker app, combining the Django backend and Angular frontend.

## 🚀 Quick Start with Docker Compose
You can spin up the entire app (frontend + backend) using:

To build the program:
docker-compose up

## 🐋 Prebuilt Docker Images
This project pulls from the following public images on Docker Hub:

* Frontend: r300887882/amazon-tracker-frontend
Pull directly:
docker pull r300887882/amazon-tracker-frontend:latest

* Backend: r300887882/amazon-tracker-backend
Pull directly:
docker pull r300887882/amazon-tracker-backend:latest

🌐 App Overview
* Backend (Django): Handles user registration, Amazon product scraping, watchlists, target price alerts, and automation.
* Frontend (Angular): Interface for searching, tracking, and managing products and watchlists.

🧪 Database
* The backend ships with an empty SQLite DB so each user starts with a clean slate.
