FROM golang


ENV GO111MODULE=on
RUN mkdir -p /go/src/github.com/Tarak311/infra_instigator/users


WORKDIR /go/src/github.com/Tarak311/infra_instigator/users
COPY . .

RUN go mod tidy
RUN go mod vendor
RUN go build -mod vendor -o server ./cmd/main.go

CMD [ "./server" ]
