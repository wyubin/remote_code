ARG VARIANT="3.13"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-alpine-${VARIANT}
## install system package
RUN apk add --no-cache -U make gcc musl-dev zlib-dev go
## install go package
RUN go get -u golang.org/x/tools/gopls && \
    go get -u github.com/go-delve/delve/cmd/dlv && \
    go get -u github.com/uudashr/gopkgs/cmd/gopkgs && \
    go get -u github.com/ramya-rao-a/go-outline && \
    go get -u github.com/fatih/gomodifytags && \
    go get -u github.com/josharian/impl && \
    go get -u github.com/cweill/gotests/... && \
    go get -u golang.org/x/lint/golint
