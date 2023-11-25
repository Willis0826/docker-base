FROM python:3.11
LABEL description="AWS SAM cli"
RUN apt-get update && apt-get install zip gcc musl-dev
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && ./aws/install
RUN curl -L "https://github.com/aws/aws-sam-cli/releases/download/v1.103.0/aws-sam-cli-linux-x86_64.zip" -o "aws-sam-cli.zip" \
    && unzip aws-sam-cli.zip \
    && ./install \
    && rm -rf aws-sam-cli.zip \
    && rm -rf aws-sam-cli-src \
    && rm -rf install 

RUN curl -fsSL https://deb.nodesource.com/setup_20.x | bash - \
    && apt-get install -y nodejs
RUN npm install -g typescript
RUN npm install -g esbuild
ENTRYPOINT []
