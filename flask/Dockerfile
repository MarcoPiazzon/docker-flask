# use the python3.10.12 container image+
FROM python:3.10

WORKDIR ./
ADD . ./
RUN pip install -r testreq.txt
RUN pip install uwsgi
RUN curl --create-dirs -o $HOME/.postgresql/root.crt 'https://cockroachlabs.cloud/clusters/0a79c505-e21c-47bb-9115-03756968b49c/cert'
RUN echo "DB_LINK = 'cockroachdb://marco:LxOxGTxloT8-Wt_4ITkZBg@dbprova-10626.7tc.aws-eu-central-1.cockroachlabs.cloud:26257/defaultdb?sslmode=verify-full'" > .env
CMD ["uwsgi", "app.ini"]


