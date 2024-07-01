# Use the official Python base image
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app

# Copy requirements.txt from your host to /app in the container
COPY requirements.txt .

# Update package index and install Python 3 and pip
RUN apt-get update && \
    apt-get install -y python3 python3-pip

# Install Python dependencies from requirements.txt
RUN pip install -r requirements.txt

# Copy the contents of the 'devops' directory from your host to /app in the container
COPY devops /app/devops

# Set the default command to run when the container starts
CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]
