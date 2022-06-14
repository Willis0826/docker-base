FROM python:3
LABEL description="GCP terraform"

RUN curl -o "terraform_1.2.2_linux_amd64.zip" -l https://releases.hashicorp.com/terraform/1.2.2/terraform_1.2.2_linux_amd64.zip && \
  unzip terraform_1.2.2_linux_amd64.zip && \
  mv terraform /bin/terraform && \
  rm -rf terraform_1.2.2_linux_amd64.zip


RUN curl -o "google-cloud-cli-389.0.0-linux-x86_64.tar.gz" -l https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-cli-389.0.0-linux-x86_64.tar.gz && \
  tar xvzf google-cloud-cli-389.0.0-linux-x86_64.tar.gz && \
  ./google-cloud-sdk/install.sh --quiet && \
  rm -rf google-cloud-cli-389.0.0-linux-x86_64.tar.gz

ENV PATH="${PATH}:/google-cloud-sdk/bin"