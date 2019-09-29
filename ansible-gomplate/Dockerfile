FROM python:3.7-slim
LABEL description="Ansible and gomplate deployment"
RUN apt-get update \
    && apt-get -y install curl \
    && apt-get -y install ansible \
    && curl -L -o /usr/local/bin/gomplate https://github.com/hairyhenderson/gomplate/releases/download/v3.5.0/gomplate_linux-amd64 \
    && chmod +x /usr/local/bin/gomplate

ENTRYPOINT ["/bin/bash", "-l", "-c"]
