FROM alpine:latest

RUN apk --no-cache add git curl jq github-cli \
    && rm -rf /var/lib/apt/lists/*

RUN curl -LO https://github.com/BenGercuj/changelog-from-release/releases/download/v1.0.0/changelog-from-release_1.0.0_linux_amd64.tar.gz \
    && tar xf changelog-from-release_1.0.0_linux_amd64.tar.gz -C / \
    && rm changelog-from-release_1.0.0_linux_amd64.tar.gz

COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
