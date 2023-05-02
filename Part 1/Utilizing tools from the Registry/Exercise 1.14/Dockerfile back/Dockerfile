FROM golang:1.16

WORKDIR /usr/src/app

COPY . .

RUN go build
RUN go test ./...
#RUN ./server

ENV PORT 8080
ENV REQUEST_ORIGIN http://192.168.56.11

EXPOSE 8080

CMD ["./server"]