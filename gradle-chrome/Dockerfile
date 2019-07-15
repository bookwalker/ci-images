FROM gradle:5.5-jdk11

USER root

RUN apt-get update && \
    apt-get -y install curl && \
    apt-get -y install gnupg && \
    apt-get -y install rsync && \
    apt-get -y install git

# install chrome headless
RUN curl -sS https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add
RUN echo 'deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main' |  tee /etc/apt/sources.list.d/google-chrome.list
RUN apt-get update
RUN apt-get install google-chrome-stable -y

# install chromium headless
#RUN apt-get -y install software-properties-common && \
#    add-apt-repository ppa:canonical-chromium-builds/stage && \
#    apt-get update && \
#    apt-get -y install chromium-browser

USER gradle
