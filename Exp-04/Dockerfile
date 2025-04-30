# Use Python as base image
FROM python:3-slim

# Set working directory
WORKDIR /app

# Copy application files
COPY . .

# Install dependencies
RUN pip install --no-cache-dir streamlit psycopg2-binary


# Expose Streamlit port
EXPOSE 8504

# Run Streamlit
CMD ["streamlit", "run", "stream.py", "--server.port=8504", "--server.address=0.0.0.0"]
