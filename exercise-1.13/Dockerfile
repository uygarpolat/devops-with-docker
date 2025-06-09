FROM golang:1.16

WORKDIR /mybackend

COPY . .

RUN go build .

EXPOSE 8080

CMD ["./server"]