# Install golang 1.16
FROM golang:1.16-alpine

EXPOSE 8080

WORKDIR /usr/src/app
# Copy source code
COPY . .

ENV REQUEST_ORIGIN=http://localhost:5000

ENV GOPATH=/go
# Build project to create binary server
RUN go build

# We don't need to test project like README and move on to execute project
CMD ["./server"]
