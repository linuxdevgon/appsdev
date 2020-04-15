FROM python:3.8.0-alpine
RUN pip install --upgrade pip

RUN mkdir /app

WORKDIR /app

ADD . .

RUN pip install -r requirements.txt
CMD gunicorn app:app --bind 0.0.0.0:8000 --reload
