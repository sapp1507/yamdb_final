FROM python:3.7-slim

COPY api_yamdb/requirements.txt /app/

RUN pip install -r ./requirements.txt --no-cache-dir --upgrade pip

COPY ./ /app/
WORKDIR /app


CMD ["gunicorn", "--bind", ":8000", "api_yamdb.wsgi:application"]
