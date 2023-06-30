FROM python:3.9

WORKDIR /app

RUN pip install \
    mlflow \
    psycopg2 \
    boto3

RUN mkdir /mlflow/ && \
    mkdir --parents /data/artifacts/ && \
    chmod 777 /data/artifacts
