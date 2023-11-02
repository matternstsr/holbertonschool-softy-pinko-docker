# Use the latest Ubuntu as the base image
FROM ubuntu:latest

# Update APT repositories and upgrade installed software
RUN apt-get update -y && apt-get upgrade -y

# Install Python 3 and pip3
RUN apt-get install -y python3 python3-pip

# Install Flask using pip3
RUN pip install Flask

# Create a directory for your app
WORKDIR /app

# Copy the Python script into the Docker image
COPY api.py /app

# Expose port 5252 for the Flask application
EXPOSE 5252

# Run the Flask application when the container starts
CMD ["python3", "api.py"]
