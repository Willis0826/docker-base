# Usage

The Dockerfile provide a CI/CD running environment with kubectl & gomplate & gcloud cli and kops. Follow the step to rebuild.

1. docker build -t <docker_hub>/gcp-gomplate-kubectl:<image_tag> .

2. docker push <docker_hub>/gcp-gomplate-kubectl:<image_tag>

## Docker Image

willischou/gcp-gomplate-kubectl:0.3
