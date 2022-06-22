FROM n8nio/n8n:0.172.0
RUN apk add --update python3 py3-pip

ENV APP_HOME /apisifyflow
WORKDIR $APP_HOME
COPY . $APP_HOME

ENV DB_TYPE=mysqldb
ENV DB_MYSQLDB_DATABASE=mysqldb
ENV DB_MYSQLDB_HOST=mysqldb
ENV DB_MYSQLDB_PORT=3306

RUN pip install -r requirements.txt

RUN mkdir -p /data/.n8n/
RUN mv -n ./.n8n/config.json /data/.n8n/.

ENV N8N_CONFIG_FILES /data/.n8n/config.json
