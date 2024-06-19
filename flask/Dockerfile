FROM python:3.8-alpine

WORKDIR /app

COPY . /app

RUN pip install --no-cache-dir Flask gunicorn

ENV PORT=8080

CMD gunicorn --bind 0.0.0.0:$PORT app.main:app


