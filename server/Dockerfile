FROM registry.opensource.zalan.do/stups/openjdk:latest

MAINTAINER "http://zalando.github.io/"

COPY build/libs/zally-1.0.0.jar /

EXPOSE 8080

CMD java $(java-dynamic-memory-opts) $(appdynamics-agent) -jar /zally-1.0.0.jar
