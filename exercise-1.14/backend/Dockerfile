FROM golang:1.16

WORKDIR /mybackend

COPY . .

ENV REQUEST_ORIGIN=http://127.0.0.1:5000

RUN go build .

EXPOSE 8080

CMD ["./server"]