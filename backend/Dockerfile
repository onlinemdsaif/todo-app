# Use Python image
FROM python:3.9

# Set working directory
WORKDIR /app

# Copy requirements and install dependencies
COPY requirements.txt .
RUN pip install -r requirements.txt

# Copy the rest of the app files
COPY . .

# Expose the application port
EXPOSE 5000

# Start the Flask app
CMD ["python", "app.py"]
