FROM golang:1.19-alpine

WORKDIR /app

COPY go.mod go.sum ./ # ---> instead of copying all files we are copying only files req for downloading dependencies

RUN go mod download

COPY . .

RUN go build -o api-golang # ---> we are creating binary and we execute evertime this binary

CMD ["./api-golang"]