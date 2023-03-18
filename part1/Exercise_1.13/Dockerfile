FROM golang:alpine
RUN mkdir /opt/app
COPY example-backend/ /opt/app/
WORKDIR /opt/app
RUN go build
ENV PORT 8000
ENV REQUEST_ORIGIN http://localhost:5000
EXPOSE 8000
RUN chmod +x server
CMD ["./server"]
#ENTRYPOINT [ "/bin/sh" ]