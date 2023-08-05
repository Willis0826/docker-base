# Usage

The Dockerfile provide a AWS SAM CLI 1.94.0 to build and deploy AWS serverless application.
Also, this image includes nodejs 18 runtime and typescript.

Build AMD64:

1. docker buildx build --load --platform=linux/amd64 -t willischou/sam:release-0.5.0 .

2. docker push willischou/sam:release-0.5.0

Build ARM64:

1. docker buildx build --load --platform=linux/arm64 -t willischou/sam:release-0.5.0 .

2. docker push willischou/sam:release-0.5.0

## Docker Image

willischou/sam:release-0.5.0
