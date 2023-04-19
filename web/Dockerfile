FROM python:3.9.16-slim

ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1

RUN apt-get update && apt-get install -y \
  dos2unix \
  libpq-dev \
  libmariadb-dev-compat \
  libmariadb-dev \
  gcc \
  && apt-get clean

WORKDIR /usr/src/app

COPY ./django_blog/requirements.txt .

RUN python -m pip install --upgrade pip && python -m pip install -r requirements.txt

COPY . .
