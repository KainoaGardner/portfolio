FROM golang:1.23-alpine

WORKDIR /app

COPY go.mod .
COPY go.sum .
RUN go mod download

COPY . .

RUN go build -o /app/cmd/main /app/cmd/main.go
EXPOSE 3000

CMD ["/app/cmd/main"]
