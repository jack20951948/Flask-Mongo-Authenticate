FROM python:3.12.1-slim

RUN echo "WORKDIR /api"
WORKDIR /api

RUN echo "COPY . ."
COPY . .

RUN echo "RUN pip3 install -r requirements.txt"
RUN pip3 install -r requirements.txt

RUN echo "CMD gunicorn --bind 0.0.0.0:5000 run:app"
CMD gunicorn --bind 0.0.0.0:5000 run:app
