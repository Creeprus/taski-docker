FROM python:3.10

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt --no-cache-dir
RUN pip install gunicorn
COPY . .

CMD ["python", "manage.py", "runserver", "0:8000"] 
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]

