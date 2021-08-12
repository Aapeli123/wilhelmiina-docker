FROM golang
WORKDIR /go/src/github.com/Aapeli123/
RUN git clone https://github.com/Aapeli123/wilhelmiina-api
WORKDIR /go/src/github.com/Aapeli123/wilhelmiina-api
RUN go get -d -v ./...
RUN go build .
EXPOSE 8080
CMD ["./wilhelmiina-api"]