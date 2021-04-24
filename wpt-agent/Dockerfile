FROM webpagetest/agent:latest
RUN apt-get update && \
    apt-get install --yes --no-install-recommends \
            fonts-noto-cjk \
    && rm -rf /var/lib/apt/lists/*
    
RUN apt install xvfb -y
ADD xvfb -ac :99 -screen 0 1280x1024x16 & export DISPLAY=:99

ADD startup.sh /
RUN chmod u+x /startup.sh
ENTRYPOINT /startup.sh
