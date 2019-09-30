FROM jfloff/alpine-python:3.7-slim
LABEL description="Ansible and gomplate deployment"
RUN apk update \
    && apk add curl \
    && apk add ansible \
    && curl -L -o /usr/local/bin/gomplate https://github.com/hairyhenderson/gomplate/releases/download/v3.5.0/gomplate_linux-amd64 \
    && chmod +x /usr/local/bin/gomplate

ENTRYPOINT ["/bin/bash", "-l", "-c"]
