# Usage

The Dockerfile provide a CI/CD running environment with awscli, gomplate and terraform 0.12.18 based on ubuntu:18.04, Follow the step to rebuild.

1. docker build -t <docker_hub>/gomplate-terraform:<image_tag> .

2. docker push <docker_hub>/gomplate-terraform:<image_tag>

## Docker Image

willischou/gomplate-terraform:0.3
