FROM bitnami/golang:latest as base

WORKDIR /frontend

COPY . .

RUN go build -o klijent

#RUN chmod +x entry.sh

EXPOSE 8090

ENTRYPOINT ["./klijent"]