FROM python:3.6.5-slim
#just a means to putless image footprint
RUN apt-get update

WORKDIR /code

RUN pip install --upgrade pip

COPY . /code

CMD ["bash"]
