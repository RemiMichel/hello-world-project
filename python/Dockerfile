FROM python:latest

COPY . /application

WORKDIR /application

RUN --mount=type=cache,target=/root/.cache/pip \
    pip3 install -r requirements.txt

ENV FLASK_APP main.py
ENV FLASK_ENV development
ENV FLASK_RUN_PORT 8000
ENV FLASK_RUN_HOST 0.0.0.0

EXPOSE 8000

CMD ["flask", "run"]