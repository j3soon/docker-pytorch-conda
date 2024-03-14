# Docker image for PyTorch with conda

[<img src="https://img.shields.io/badge/dockerhub-image-important.svg?logo=docker">](https://hub.docker.com/r/j3soon/pytorch-conda/tags)

A quick reference for setting up conda on custom base image. This may be useful since PyTorch NGC container after 22.11 does not contain miniforge (a minimal conda distribution) anymore.

> Starting with the 22.11 PyTorch NGC container, miniforge is removed and all Python packages are installed in the default Python environment.
>
> -- [PyTorch Release Notes](https://docs.nvidia.com/deeplearning/frameworks/pytorch-release-notes/rel-22-11.html)

## Run the pre-built Docker Image

```sh
docker run --rm -it --gpus all j3soon/pytorch-conda:23.12-py3
conda -V
```

The [pre-built docker images](https://hub.docker.com/r/j3soon/ros-humble-desktop-full/tags) will be pulled automatically.

## Build Docker Images Locally

```sh
git clone https://github.com/j3soon/docker-pytorch-conda.git
cd docker-pytorch-conda
docker build -t j3soon/pytorch-conda:23.12-py3 .
```
