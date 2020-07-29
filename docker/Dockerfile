FROM alpine:latest as alpine
RUN apk add -U --no-cache ca-certificates

ARG PKG_FILES
FROM scratch
ENTRYPOINT []
ADD . ./dist
WORKDIR /
COPY --from=alpine /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/
COPY $PKG_FILES /
