FROM python:3.9.12-bullseye

ENV APP_HOME /apisifyview
WORKDIR $APP_HOME
COPY . $APP_HOME

RUN pip install -r requirements.txt

CMD ["streamlit", "run", "main.py", "--server.port", "8501"]
