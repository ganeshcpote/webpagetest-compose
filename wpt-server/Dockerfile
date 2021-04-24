FROM webpagetest/server:latest
RUN apt-get update && \
    apt-get install --yes --no-install-recommends \
             php7.2-apcu \
    && apt-get install --yes \
               python-dev \
               python-pip \
    && rm -rf /var/lib/apt/lists/*
RUN apt-get -y install gcc make autoconf libc-dev pkg-config
RUN apt install xvfb -y
ADD Xvfb -ac :99 -screen 0 1280x1024x16 & export DISPLAY=:99
RUN pip install pyssim
