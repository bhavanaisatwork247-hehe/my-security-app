FROM python:3.10-slim

WORKDIR /app

# Install security tools like Semgrep & Git
RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*
RUN pip install --no-cache-dir semgrep fastapi uvicorn

# Copy app code
COPY . .

EXPOSE 8003

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8003"]