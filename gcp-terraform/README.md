# Usage

The Dockerfile provide a CI/CD running environment with terraform & gcloud cli. Follow the step to rebuild.

1. docker build .

2. docker tag <image_id> <docker_hub>/gcp-terraform:<image_tag>

3. docker push <docker_hub>/gcp-terraform:<image_tag>

## Docker Image

willischou/gcp-terraform:0.5
