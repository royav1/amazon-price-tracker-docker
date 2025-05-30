# backend/Dockerfile

FROM python:3.11-slim

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Create working directory
WORKDIR /app

# Install system dependencies
RUN apt-get update && apt-get install -y \
    build-essential \
    libpq-dev \
    curl \
    wget \
    && apt-get clean

# Install Python dependencies
COPY requirements.txt .
RUN pip install --upgrade pip && pip install -r requirements.txt

# ✅ Install Playwright browser binaries
RUN playwright install --with-deps

# Copy project files
COPY . .

# Expose port for Django dev server
EXPOSE 8000

# Start the development server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
