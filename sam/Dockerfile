FROM python:3.9.4
LABEL description="AWS SAM cli"
# use google dns
RUN echo "nameserver 8.8.8.8" > /etc/resolv.conf
RUN apt-get update && apt-get install zip gcc musl-dev
RUN pip install aws-sam-cli
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && ./aws/install
ENTRYPOINT ["/bin/sh", "-l", "-c"]
