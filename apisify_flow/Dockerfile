FROM n8nio/n8n
RUN apk add --update python3 py3-pip

ENV APP_HOME /apisifyflow
WORKDIR $APP_HOME
COPY . $APP_HOME

ENV N8N_CONFIG_FILES /data/.n8n/config.json

ENV DB_TYPE=mysqldb
ENV DB_MYSQLDB_DATABASE=mysqldb
ENV DB_MYSQLDB_HOST=mysqldb
ENV DB_MYSQLDB_PORT=3306

RUN pip install -r requirements.txt