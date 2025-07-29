FROM golang:1.23.5-alpine3.21 AS builder

WORKDIR /app
COPY main.go .
RUN go build -o main main.go

FROM alpine:3.21

WORKDIR /app
COPY --from=builder /app/main .

CMD ["./main"]
