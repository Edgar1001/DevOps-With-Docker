FROM alpine:latest

# app runs on port 8080
EXPOSE 8080

WORKDIR /usr/src/app

# install go
RUN apk add --no-cache go

# copy sources
COPY . .


# run installer
RUN go build

# add user to alpine
RUN addgroup -S newgroup && adduser -S newuser -G newgroup

# run as non-root user
USER newuser

ENTRYPOINT ["./server"]
