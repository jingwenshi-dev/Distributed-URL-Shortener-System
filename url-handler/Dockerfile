FROM python:3.11-slim

WORKDIR /app
ADD . /app

RUN pip install --trusted-host pypi.python.org -r requirements.txt
RUN apt-get update
RUN apt-get install -y curl
RUN apt-get clean
RUN rm -rf /var/lib/apt/lists/*

EXPOSE 80

CMD ["python", "app.py"]
