FROM python:3.7
WORKDIR /app
COPY requirements.txt ./
RUN python3 -m pip install --upgrade pip && pip install -r requirements.txt
COPY . .
EXPOSE 5000
##CMD ["gunicorn","--workers-1", "--bind", "0.0.0.0:5000", "-c", "config.py", "app:app"]
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "-c", "config.py", "app:app"]
