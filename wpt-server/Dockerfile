FROM webpagetest/server:latest
RUN apt-get update && \
    apt-get install --yes \
               python-dev \
               python-pip \
    && rm -rf /var/lib/apt/lists/*
RUN apt-get -y install gcc make autoconf libc-dev pkg-config
RUN pip install pyssim
