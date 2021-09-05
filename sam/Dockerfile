FROM python:3.9.4
LABEL description="AWS SAM cli"
RUN apt-get update && apt-get install zip gcc musl-dev
RUN pip install aws-sam-cli
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && ./aws/install
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -
RUN apt-get install -y nodejs
RUN npm install -g typescript
ENTRYPOINT []
