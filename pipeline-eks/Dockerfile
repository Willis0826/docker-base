FROM seitk/pipeline-eks AS builder
# gomplate
RUN curl -LO https://github.com/hairyhenderson/gomplate/releases/download/v3.6.0/gomplate_linux-amd64-slim \ 
    && chmod +x ./gomplate_linux-amd64-slim \
    && mv ./gomplate_linux-amd64-slim /usr/local/bin/gomplate
# helm v3.2.4
RUN curl -LO https://get.helm.sh/helm-v3.2.4-linux-amd64.tar.gz \
    && tar -xvf helm-v3.2.4-linux-amd64.tar.gz \
    && mv ./linux-amd64/helm /usr/local/bin/helm3
# git crypt
RUN apk add --update alpine-sdk make libressl-dev
RUN git clone https://github.com/AGWA/git-crypt.git \
    && cd git-crypt \
    && make \
    && make install PREFIX=/usr/local

FROM seitk/pipeline-eks
# git crypt require duplicity (gpg)
RUN apk add duplicity
COPY --from=builder /usr/local/bin/gomplate /usr/local/bin/gomplate
COPY --from=builder /usr/local/bin/helm3 /usr/local/bin/helm3
COPY --from=builder /usr/local/bin/git-crypt /usr/local/bin/git-crypt