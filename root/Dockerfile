FROM node:12

COPY . /app
WORKDIR /app

RUN \
  export DEBIAN_FRONTEND=noninteractive && \
  apt update && \
  apt upgrade -y && \
  apt install -y tree && \
  pwd && \
  tree && \
  npm install && \
  npm run print-http-server-version

EXPOSE 8080

CMD ["npm", "start"]