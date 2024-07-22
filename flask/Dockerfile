# use the python3.10.12 container image+
FROM python:3.10.12-stretch

WORKDIR .
ADD . /app
RUN pip install -r requirements.txt
CMD ["uwsgi", "app.ini"]


