FROM python:3.11
LABEL description="AWS SAM cli"
RUN apt-get update && apt-get install zip gcc musl-dev
RUN pip install aws-sam-cli
RUN curl -L "https://github.com/aws/aws-sam-cli/releases/download/v1.94.0/aws-sam-cli-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && ./install \
    && rm -rf awscliv2.zip \
    && rm -rf aws-sam-cli-src \
    && rm -rf install 

RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - \
    && apt-get install -y nodejs
RUN npm install -g typescript
RUN npm install -g esbuild
ENTRYPOINT []
