# Use a specific Python image as the base
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy only requirements to leverage Docker cache
COPY requirements.txt .

# Install dependencies, with retries in case of network timeouts
RUN pip install  -r requirements.txt

# Copy the rest of the application code
COPY . .

# Specify the command to run the app (update if different)
CMD ["python", "app.py"]
