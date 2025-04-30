# Use a lightweight Python image
FROM python:3-slim

# Keeps Python from generating .pyc files
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Install dependencies
COPY requirements.txt .
RUN pip install -r requirements.txt

# Set working directory
WORKDIR /app
COPY . /app

# Ensure Streamlit runs as non-root user
RUN adduser --disabled-password --gecos "" appuser && chown -R appuser /app
USER appuser

# Expose the Streamlit default port
EXPOSE 8502

# Run Streamlit
CMD ["streamlit", "run", "app.py","--server.port=8502", "--server.address=0.0.0.0"]
