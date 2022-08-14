FROM python:3.7-slim

COPY ./api_yamdb /app

COPY requirements.txt .

RUN python -m pip install --upgrade pip

RUN pip3 install -r /app/requirements.txt --no-cache-dir

WORKDIR /app/

CMD ["gunicorn", "api_yamdb.wsgi:application", "--bind", "0:8000" ]
