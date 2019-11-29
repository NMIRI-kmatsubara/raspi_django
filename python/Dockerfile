FROM nmirikm/raspi_python:3.6.5
ENV PYTHONUNBUFFERED 1
RUN apt-get update && \
    echo "mysql-server mysql-server/root_password password root" | debconf-set-selections && \
    echo "mysql-server mysql-server/root_password_again password root" | debconf-set-selections && \
    apt-get install -y \
    build-essential \
    python-dev \
    mysql-server \
    libmysqlclient-dev 
RUN mkdir /code
WORKDIR /code
ADD requirements.txt /code/
RUN pip install -r requirements.txt
ADD . /code/
