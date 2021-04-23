FROM golang as builder

COPY ./src /go/src/
RUN go build src/main.go

FROM scratch
COPY --from=builder /go/main .
CMD ["./main"]