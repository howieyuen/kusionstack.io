---
sidebar_position: 1
---

# Installation Guide

## Homebrew (MacOS & Linux)

The preferred method for installing on Mac and Linux is to use the brew package manager.

You can install the latest Kusion CLI with the following:

```bash
brew install KusionStack/tap/kusion
```

You can also follow the binary installation below.

## Curl|sh install (MacOS & Linux)

If you don't have homebrew, you can install the CLI with this one-liner:

```bash
curl https://kusionstack.io/scripts/install.sh | sh
```

## Powershell (Windows)

Run the following command in *powershell* with administrator privilege.

```bash
powershell -Command "iwr -useb https://kusionstack.io/script/install.ps1 | iex"
```

## Manual install

You can download the Kusion CLI binary from the project's [GitHub page](https://github.com/KusionStack/kusion/releases/). 

Download the tar.gz archive for your machine, uncompress and move the binary to your PATH.

```bash
tar -zxvf ~/Downloads/kusion_<VERSION>_<OS>_<ARCH>.tar.gz
mv ~/Downloads/kusion /usr/local/bin
```

:::info
If *golang* isn't installed, please add `/root/go/bin` to your `PATH`.
Otherwise, make sure that `$GOPATH/bin` is in your `PATH`.
:::

Kusion CLI don't support Windows for now, we are working on it and will support Windows as soon as possible.

## Docker Image

If the upper installation doesn't support your environment, you can use the docker image of Kusion instead.

First, pull the latest image:

```bash
docker pull kusionstack/kusion:latest
```

Next, run Kusion in an interactive mode:

```bash
docker run --rm -it kusionstack/kusion:latest bash
```
