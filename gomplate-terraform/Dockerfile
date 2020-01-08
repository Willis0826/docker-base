FROM ubuntu:18.04
LABEL description="Ubuntu 18 based with awscli, gomplate and terraform executable"
RUN apt-get -y update && apt-get install -y git lftp openssh-client coreutils curl unzip python-pip
RUN curl -LO https://github.com/hairyhenderson/gomplate/releases/download/v3.6.0/gomplate_linux-amd64-slim \ 
    && chmod +x ./gomplate_linux-amd64-slim && mv ./gomplate_linux-amd64-slim /bin/gomplate \
    && curl -LO https://releases.hashicorp.com/terraform/0.12.18/terraform_0.12.18_linux_amd64.zip \
    && unzip ./terraform_0.12.18_linux_amd64.zip \
    && chmod +x ./terraform && mv ./terraform /bin/terraform \
    && rm ./terraform_0.12.18_linux_amd64.zip \
    && curl -sSL https://get.docker.com/ | sh
RUN pip install awscli

ENTRYPOINT ["/bin/bash", "-l", "-c"]