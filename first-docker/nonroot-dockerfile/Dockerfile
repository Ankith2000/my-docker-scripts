##########################################
# 08. Non-root User Dockerfile
##########################################
FROM python:3.12-slim
RUN useradd -m appuser
WORKDIR /app
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
USER appuser
EXPOSE 5000
CMD ["python", "app.py"]