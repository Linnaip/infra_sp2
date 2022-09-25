FROM python:3.9-slim

RUN mkdir /app

COPY requirements.txt /app

RUN pip3 install -r /app/requirenents.txt --no-cache-dir

COPY api_yamdb/ /app

WORKDIR /app

CMD ["python3", "manage.py", "runserver", "0:8000"]
