FROM node:current-alpine3.10

LABEL maintainer="mueee"

#RUN apt-get install -y git
RUN apk add --no-cache \
git \
curl \
python \
make \
gcc \
libc-dev \
g++

#RUN npm install

#RUN npm install -g node-pre-gyp

RUN git clone https://github.com/UnicornTranscoder/UnicornLoadBalancer.git
WORKDIR ./UnicornLoadBalancer

RUN npm install

ENV PLEX_HOST 127.0.0.1
ENV PLEX_PORT 32400
ENV PLEX_PATH_USR /usr/lib/plexmediaserver/
ENV PLEX_PATH_SESSIONS /var/lib/plexmediaserver/Library/Application Support/Plex Media Server/Cache/Transcode/Sessions

EXPOSE 32400/tcp

ENTRYPOINT ["npm start"]
