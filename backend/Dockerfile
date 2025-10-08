FROM python:3.13-alpine3.22

WORKDIR /backend

COPY requirements.txt .

RUN pip install --upgrade pip && \
    pip install -r requirements.txt

COPY . .
