FROM nmirikm/raspi_python:3.6.5
ENV PYTHONUNBUFFERED 1
RUN apt-get update && apt-get install -y \
    build-essential \
    python-dev
RUN mkdir /code
WORKDIR /code
ADD requirements.txt /code/
RUN pip install -r requirements.txt
ADD . /code/
