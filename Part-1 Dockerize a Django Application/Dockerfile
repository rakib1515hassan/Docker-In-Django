# Use the official Python image from the Docker Hub
FROM python:3.11-slim


# Set the working directory
WORKDIR /app


# Install dependencies
RUN apt-get update \
    && apt-get install -y --no-install-recommends gcc libpq-dev \
    && pip install --upgrade pi



# Copy the requirements file
# COPY requirements.txt /app/
COPY requirements.txt requirements.txt



# Install Python dependencies
RUN pip3 install -r requirements.txt



# Copy the application code
# COPY . /app/
COPY . .



# Specify the default command to run the application
CMD [ "python3", "manage.py", "runserver", "0.0.0.0:8000"]



# Expose the port the app runs on
# EXPOSE 8000