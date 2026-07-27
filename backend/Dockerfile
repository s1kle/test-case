FROM python:3.12-alpine

ENV PORT=8080
ENV HOST=0.0.0.0
ENV PYTHONUNBUFFERED=1
ENV PYTHONDONTWRITEBYTECODE=1

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

RUN adduser -D backend
USER backend

COPY main.py .

EXPOSE ${PORT}

CMD uvicorn main:app --host ${HOST} --port ${PORT}