
ARG PYTHON_VERSION=3.9.0
FROM quay.io/mlrun/python:3.9.13-slim as base

ENV PYTHONDONTWRITEBYTECODE=1

ENV PYTHONUNBUFFERED=1

WORKDIR /backend

RUN --mount=type=cache,target=/root/.cache/pip \
    --mount=type=bind,source=requirements.txt,target=requirements.txt \
    python -m pip install -r requirements.txt

COPY . .

EXPOSE 8000

CMD uvicorn 'main:app' --host=0.0.0.0 --port=8000
