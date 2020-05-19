FROM python:3.7.4

RUN mkdir -p /var/www

WORKDIR /var/www

COPY requirements.txt ./

RUN pip install -U pip setuptools && \
    pip install --no-cache-dir -r requirements.txt

RUN ls

WORKDIR /var/www/DockerTest

CMD ["uwsgi", "--ini", "/var/www/uwsgi.ini"]