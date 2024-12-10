# Use the official Python image
FROM python:3.11-slim

# Set the working directory
WORKDIR /app

# Copy requirements file and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application code
COPY . .

# Expose the port and run with gunicorn
EXPOSE 5009
CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:5009", "app:app"]
