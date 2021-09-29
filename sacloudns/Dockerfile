FROM golang:alpine as builder
RUN apk add git
RUN git clone https://github.com/sacloud/sacloudns.git -b v0.0.6 --depth 1
WORKDIR sacloudns
RUN go build -o /sacloudns -ldflags '-w -s -X main.version=v0.0.6'

FROM alpine
COPY --from=builder /sacloudns /sacloudns
ENTRYPOINT ["/sacloudns"]
