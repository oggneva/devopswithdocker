FROM ubuntu:16.04

RUN apt-get update && \
    apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs

WORKDIR /app
COPY . /app

ENV API_URL=http://localhost:8000

RUN npm install && \
    npm run build 

EXPOSE 5000

ENTRYPOINT ["npm", "run", "start-built"]