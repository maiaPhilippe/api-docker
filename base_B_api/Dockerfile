FROM python:3.6-alpine3.6

ENV GUNICORN_N_WORKERS 9
ENV GUNICORN_W_TIMEOUT 60
ENV FLASK_APP=run.py
ENV FLASK_ENV=development
ENV APP_SETTINGS=development
ENV MONGODB_URL=0.0.0.0
ENV DB_NAME=teste



ADD . /app

WORKDIR /app

RUN apk update && \
 python3 -m pip install -r requirements.txt --no-cache-dir

EXPOSE 3000

CMD ["flask", "run", "--host=0.0.0.0", "--port=3000"]
