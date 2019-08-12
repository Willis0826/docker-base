FROM jfloff/alpine-python:2.7-slim
LABEL description="GCP gomplate kubectl"
COPY ./kubectl /bin
COPY ./gomplate /bin
COPY ./google-cloud-sdk-183.0.0-linux-x86.tar.gz /
RUN tar xvzf google-cloud-sdk-183.0.0-linux-x86.tar.gz && ./google-cloud-sdk/install.sh --quiet
RUN ln -s /google-cloud-sdk/bin/gcloud /bin/gcloud
RUN apk add zip
ENTRYPOINT ["/bin/bash", "-l", "-c"]
