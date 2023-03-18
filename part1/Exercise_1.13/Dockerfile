FROM golang:alpine
RUN mkdir /opt/app
COPY example-backend/ /opt/app/
WORKDIR /opt/app
RUN go build
EXPOSE 8080
RUN chmod +x server
CMD ["./server"]
#ENTRYPOINT [ "/bin/sh" ]
