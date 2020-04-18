FROM ubuntu:16.04

RUN apt-get update && \
    apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs

WORKDIR /app
COPY . /app

RUN npm install 

EXPOSE 8000

ENTRYPOINT ["npm", "start"]