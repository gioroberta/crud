FROM ubuntu:latest AS build

RUN apt-get update
RUN apt-get instal openjdk-11-jdk -y
COPY . .

RUN apt-get install maven -y
RUN mvn clean install

FROM openjdk:11-jdk-slim

EXPOSE 8080
