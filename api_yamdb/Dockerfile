FROM python:3.7-slim

COPY ./ /app

RUN pip install pip --upgrade
RUN pip install -r /app/requirements.txt --no-cache-dir

WORKDIR /app

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000"]
