# Use the official Python image from Docker Hub
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app-container

# Copy the requirements.txt into the container
COPY requirements.txt /app-container/

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the entire Flask project into the container
COPY . /app-container/

# Expose port 5000, which is the default for Flask
EXPOSE 5000

# Set the environment variable to tell Flask the app is in production
ENV FLASK_ENV=production

# Set the command to run the Flask app
CMD ["flask", "run", "--host=0.0.0.0"]
