FROM        python:3.8-slim-buster
WORKDIR     /app
COPY        requirements.txt .
RUN         pip install -r requirements.txt
COPY        . .
ENTRYPOINT [ "gunicorn", "--workers=3", "--bind", "0.0.0.0:5000", "app:app" ]
EXPOSE      5000
