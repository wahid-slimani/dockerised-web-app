FROM python:3.9-slim
WORKDIR /app
COPY . .
# Increase pip timeout and use no-cache-dir to avoid caching
RUN pip install --default-timeout=100  -r requirements.txt
EXPOSE 8080
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8080"]
