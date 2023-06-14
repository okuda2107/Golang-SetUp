FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu-20.04

ARG GO_VERSION=1.19
RUN set -x \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
    build-essential \
    curl \
    git \
    && apt-get clean && rm -rf /var/cache/apt/archives/* /var/lib/apt/lists/* \
    && curl -fsSL "https://dl.google.com/go/go${GO_VERSION}.linux-amd64.tar.gz" | tar -xz -C /usr/local
ENV GOROOT=/usr/local/go \
    GOPATH=/home/vscode/go \
    PATH=/home/vscode/go/bin:/usr/local/go/bin:${PATH}
