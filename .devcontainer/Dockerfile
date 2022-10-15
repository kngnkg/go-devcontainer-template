FROM golang:latest

RUN apt update

# Module ModeをONにする
ENV GO111MODULE on

# Remote Containerがデフォルトで開くディレクトリは/workspaceなので変更
WORKDIR /go/src/app

# install go tools
RUN go install github.com/uudashr/gopkgs/v2/cmd/gopkgs@latest && \ 
    go install -v github.com/go-delve/delve/cmd/dlv@latest && \
    go install github.com/ramya-rao-a/go-outline@latest && \
    go install github.com/stamblerre/gocode@latest && \
    go install github.com/acroca/go-symbols@latest && \
    go install github.com/fatih/gomodifytags@latest && \
    go install github.com/josharian/impl@latest && \
    go install golang.org/x/tools/gopls@latest && \
    go install github.com/haya14busa/goplay/cmd/goplay@latest && \
    go install honnef.co/go/tools/cmd/staticcheck@latest