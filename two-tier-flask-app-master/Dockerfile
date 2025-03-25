# Stage 1: Build dependencies in a separate stage
FROM python:3.9 AS builder

WORKDIR /app

# Install dependencies inside a virtual environment to reduce final image size
COPY requirements.txt .
RUN python -m venv venv && \
    . venv/bin/activate && \
    pip install --no-cache-dir -r requirements.txt

# Stage 2: Production-ready lightweight image
FROM python:3.9-slim

WORKDIR /app

# Copy only necessary files from the builder stage
COPY --from=builder /app/venv /app/venv
COPY . .

# Ensure dependencies are used from the virtual environment
ENV PATH="/app/venv/bin:$PATH"

# Expose the port and run the Flask app
EXPOSE 5000
CMD ["python", "app.py"]
