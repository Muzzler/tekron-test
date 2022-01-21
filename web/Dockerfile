# BUILD
FROM golang:alpine:latest as builder

COPY dispatcher.go .
RUN go build dispatcher.go

# RUN
FROM alpine

EXPOSE 808
CMD ["/dispatcher"]

COPY --from=builder /go/dispatcher /
COPY static /static/
