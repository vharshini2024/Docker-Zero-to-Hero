# Use the official Ubuntu base image
FROM ubuntu

# Set the working directory inside the container
WORKDIR /app

# Copy requirements.txt from your host to /app in the container
COPY requirements.txt /app

# Copy the contents of the 'devops' directory from your host to /app in the container
COPY devops /app

# Update package index and install Python 3 and pip
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip install -r requirements.txt

# Set the default command to run when the container starts
ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]
