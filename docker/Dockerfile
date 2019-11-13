FROM tensorflow/tensorflow:latest-py3

MAINTAINER Walter Lucas - Research in Software Engineering Department of University of Brasília.

RUN apt-get update && \
    apt-get install -y nodejs npm git libpangocairo-1.0-0 libx11-xcb1 libxcomposite1 libxcursor1 libxdamage1 libxi6 libxtst6 libnss3 libcups2 libxss1 libxrandr2 libgconf2-4 libasound2 libatk1.0-0 libgtk-3-0 && \
    cd /home && \
    git clone https://github.com/nanohop/sketch-to-react-native.git && \
    cd sketch-to-react-native && \
    npm install && \
    npm link && \
    npm run build && \
    mkdir -p /home/sketch-to-react-native/workspace /home/sketch-to-react-native/output

COPY Launcher.js /home/sketch-to-react-native/node_modules/puppeteer/lib/

WORKDIR /home/sketch-to-react-native

EXPOSE 22
