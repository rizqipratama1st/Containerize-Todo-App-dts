# FROM ubuntu:focal
FROM node:slim

#Create Directory
RUN mkdir -v /app

# Add Client
WORKDIR /app
COPY client client
WORKDIR /app/client
EXPOSE 3000

# Add Go-Server
WORKDIR /app
RUN mkdir go-server
WORKDIR /app/go-server
COPY ./go-server/main main
EXPOSE 8080

# Start app
WORKDIR /app/client/
COPY envSetup/start-client.sh start-client.sh 
RUN chmod +x start-client.sh
WORKDIR /app/go-server/
COPY envSetup/start-go.sh start-go.sh 
RUN chmod +x start-go.sh
WORKDIR /
COPY envSetup/startup.sh startup.sh
RUN chmod +x startup.sh
CMD ./startup.sh
