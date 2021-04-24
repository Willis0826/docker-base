FROM python:3.9.4-alpine
LABEL description="AWS SAM cli"
RUN apk --update --no-cache add curl zip gcc linux-headers musl-dev
RUN pip install aws-sam-cli
ENTRYPOINT ["/bin/bash", "-l", "-c"]
