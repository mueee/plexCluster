FROM node:current-alpine3.10

LABEL maintainer="mueee"

RUN apk add --no-cache \
git 
#curl \
#python \
#make \
#gcc \
#libc-dev \
#g++

RUN git clone https://github.com/UnicornTranscoder/UnicornTranscoder.git
WORKDIR ./UnicornTranscoder

ENV SERVER_PORT 3001


RUN npm install

ENTRYPOINT ["npm", "start"]
