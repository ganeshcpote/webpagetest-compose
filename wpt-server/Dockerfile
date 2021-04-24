FROM webpagetest/server:latest
RUN apt-get update && \
    apt-get install --yes --no-install-recommends \
            php-apcu \
    && apt-get install --yes \
               python-dev \
               python-pip \
    && rm -rf /var/lib/apt/lists/*

RUN pip install pyssim
