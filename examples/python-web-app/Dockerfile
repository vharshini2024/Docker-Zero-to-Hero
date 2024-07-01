# Use a Python base image
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Update and install system dependencies
RUN apt-get update && apt-get install -y python3 python3-pip

# Copy requirements.txt and install Python dependencies
COPY requirements.txt .
RUN pip install -r requirements.txt

# Copy the contents of the 'devops' directory
COPY devops /app/devops

# Set default command
CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]
