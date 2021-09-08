FROM ubuntu:20.10

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y build-essential software-properties-common && \
    add-apt-repository --yes --update ppa:ansible/ansible && \
    apt-get install -y ansible

WORKDIR /etc/ansible

RUN useradd -ms /bin/bash operator -g operator

USER operator