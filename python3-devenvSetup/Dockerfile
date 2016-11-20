From python:3-alpine

COPY requirements.txt /home/docker-py/requirements.txt
RUN pip install -r requirements.txt

COPY test-requirements.txt /home/docker-py/test-requirements.txt
RUN pip install -r test-requirements.txt
