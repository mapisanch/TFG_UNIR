ARG BASE_CONTAINER=jupyter/minimal-notebook
FROM $BASE_CONTAINER
USER root
COPY jupyter/requirements.txt requirements.txt

# Required os libs for psycopg2
RUN apt-get update && apt-get install -y libpq-dev gcc
RUN pip install -r requirements.txt
# Switch back to jovyan to avoid accidental container runs as root
USER jovyan
