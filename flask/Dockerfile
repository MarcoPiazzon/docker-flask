# use the python3.10.12 container image+
FROM python:3.10.12

WORKDIR /
ADD . /
RUN pip install -r newreq.txt
RUN curl --create-dirs -o $HOME/.postgresql/root.crt 'https://cockroachlabs.cloud/clusters/0a79c505-e21c-47bb-9115-03756968b49c/cert'
CMD ["uwsgi", "app.ini"]


