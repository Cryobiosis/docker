#Foo
FROM ubuntu:20.04
WORKDIR /usr/src/app
COPY download.sh .
RUN chmod +x ./download.sh
RUN apt-get update && apt-get install curl -y
CMD ./download.sh
