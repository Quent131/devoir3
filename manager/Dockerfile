FROM python:latest

ADD . ./db_manager

EXPOSE 5432

RUN wget https://raw.githubusercontent.com/vishnubob/wait-for-it/master/wait-for-it.sh -P /
RUN chmod +x /wait-for-it.sh
ENTRYPOINT ["/wait-for-it.sh", "db:5432", "--"]

RUN pip install psycopg2

CMD python -m db_manager