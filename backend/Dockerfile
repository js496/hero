FROM python:3.9-slim-buster

# Set the working directory inside the container
WORKDIR /app

# Copy your application code
COPY . /app

# Ensure entrypoint.sh is copied from the root
COPY ../entrypoint.sh /app/entrypoint.sh

# Install any required dependencies
COPY requirements.txt .
RUN pip install -r requirements.txt --no-cache-dir

# Set the entrypoint
ENTRYPOINT ["/app/entrypoint.sh"]

CMD ["python", "app.py"]
