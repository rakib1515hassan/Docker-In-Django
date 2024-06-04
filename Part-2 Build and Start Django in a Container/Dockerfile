# Use the official Python image from the Docker Hub
FROM python:3.11-slim

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set the working directory
WORKDIR /myproject

# Install dependencies
RUN apt-get update \
    && apt-get install -y --no-install-recommends gcc libpq-dev \
    && pip install --upgrade pip

# Copy the requirements file
COPY requirements.txt /myproject/

# Install Python dependencies
RUN pip install -r requirements.txt

# Copy the application code
COPY . /myproject/

# Expose the port the app runs on
EXPOSE 8000

# Default command
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
