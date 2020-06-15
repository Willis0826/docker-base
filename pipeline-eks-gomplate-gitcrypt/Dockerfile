FROM seitk/pipeline-eks AS builder
# gomplate
RUN curl -LO https://github.com/hairyhenderson/gomplate/releases/download/v3.6.0/gomplate_linux-amd64-slim \ 
    && chmod +x ./gomplate_linux-amd64-slim \
    && mv ./gomplate_linux-amd64-slim /usr/local/bin/gomplate
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
COPY --from=builder /usr/local/bin/git-crypt /usr/local/bin/git-crypt
