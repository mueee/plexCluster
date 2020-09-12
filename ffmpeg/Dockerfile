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

RUN git clone https://github.com/UnicornTranscoder/UnicornFFMPEG.git
WORKDIR ./UnicornFFMPEG

RUN npm install

ENV LB_URL http://127.0.0.1/3001

ENTRYPOINT ["npm", "start"]
