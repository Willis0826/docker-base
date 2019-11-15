FROM jfloff/alpine-python:2.7-slim
LABEL description="GCP gomplate kubectl kops"
RUN apk --update add curl zip
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.16.2/bin/linux/amd64/kubectl \
    && chmod +x ./kubectl && mv ./kubectl /bin/kubectl \
    && curl -LO https://github.com/hairyhenderson/gomplate/releases/download/v3.5.0/gomplate_linux-amd64 \ 
    && chmod +x ./gomplate_linux-amd64 && mv ./gomplate_linux-amd64 /bin/gomplate \
    && curl -LO https://github.com/kubernetes/kops/releases/download/1.14.0/kops-linux-amd64 \
    && chmod +x ./kops-linux-amd64 && mv ./kops-linux-amd64 /bin/kops \
    && curl -LO https://storage.googleapis.com/cloud-sdk-release/google-cloud-sdk-183.0.0-linux-x86.tar.gz \
    && tar xvzf google-cloud-sdk-183.0.0-linux-x86.tar.gz && ./google-cloud-sdk/install.sh --quiet \
    && ln -s /google-cloud-sdk/bin/gcloud /bin/gcloud
RUN rm google-cloud-sdk-183.0.0-linux-x86.tar.gz
ENTRYPOINT ["/bin/bash", "-l", "-c"]
