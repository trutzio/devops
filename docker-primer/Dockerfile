FROM golang:1.23 AS builder
WORKDIR /src
COPY main.go main.go
RUN go build -o /bin/hello ./main.go

FROM scratch
COPY --from=builder /bin/hello /bin/hello
CMD ["/bin/hello"]