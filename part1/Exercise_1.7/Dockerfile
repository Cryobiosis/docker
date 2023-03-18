#Foo
FROM ubuntu:20.04
WORKDIR /usr/src/app
RUN apt-get update && apt-get install curl -y
COPY download.sh .
RUN chmod +x ./download.sh
#CMD ./download.sh
ENTRYPOINT [ "./download.sh" ]
