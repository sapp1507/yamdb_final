FROM python:3.7-slim

WORKDIR /app

COPY api_yamdb/requirements.txt .

RUN pip install -r ./requirements.txt --no-cache-dir --upgrade pip

COPY ./ .

CMD ["gunicorn", "--bind", ":8000", "api_yamdb.wsgi:application"]
