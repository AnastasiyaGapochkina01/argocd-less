FROM golang:1.22

WORKDIR /app

COPY go.mod ./
RUN go mod download

COPY *.go ./

RUN CGO_ENABLED=0 GOOS=linux go build -o /go-server

EXPOSE 8080

CMD [ "/go-server" ]
