# Install golang 1.16
FROM golang:1.16

EXPOSE 8080

WORKDIR /usr/src/app
# Copy source code
COPY . .

ENV REQUEST_ORIGIN=http://localhost:8080

ENV GOPATH=/go
# Build project to create binary server
RUN go build

# We don't need to test project like README and move on to execute project
CMD ["./server"]
