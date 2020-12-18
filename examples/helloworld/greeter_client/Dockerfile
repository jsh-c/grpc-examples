FROM golang:1.14.1 as builder
# RUN CGO_ENABLED=0 go get github.com/aws-samples/grpc-examples/examples/helloworld/greeter_client
RUN go build  -o /go/bin

FROM scratch
COPY --from=builder /go/bin/greeter_client /greeter_client
CMD ["/greeter_client"]

