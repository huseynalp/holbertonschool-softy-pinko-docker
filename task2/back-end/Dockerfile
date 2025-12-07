# Use the latest Ubuntu image
FROM ubuntu:latest

# Update APT and upgrade installed packages
RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y python3 python3-pip

# Fix "externally managed environment" issue
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

RUN pip3 install flask

WORKDIR /app

COPY ./api.py /app/api.py

CMD ["python3", "api.py"]
