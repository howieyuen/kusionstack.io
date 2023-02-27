---
sidebar_position: 1
---

# 安装指南

## Homebrew (MacOS & Linux)

在 Mac 和 Linux 上安装的首选方法是使用 brew 包管理器。

你可以使用以下命令安装最新的 Kusion CLI：

```bash
brew install KusionStack/tap/kusion
```

你也可以按照下面的二进制安装。

## Curl|sh (MacOS & Linux)

如果你没有 homebrew，也可以使用这个单行命令安装 CLI：

```bash
curl https://kusionstack.io/scripts/install.sh | sh
```

## Powershell (Windows)

使用管理员权限在 powershell 中运行以下命令。

```bash
powershell -Command "iwr -useb https://kusionstack.io/script/install.ps1 | iex"
```

## 手动安装

你可以从项目的 [GitHub 页面](https://github.com/KusionStack/kusion/releases/) 下载 Kusion CLI 的二进制。

下载 tar.gz 归档包到你的机器上，解压并移动到你的 `PATH` 下。

```bash
tar -zxvf ~/Downloads/kusion_<VERSION>_<OS>_<ARCH>.tar.gz
mv ~/Downloads/kusion /usr/local/bin
```

:::info
如果 *golang* 未安装，请把 `/root/go/bin` 加入到你的 `PATH`。
反之, 确保 `$GOPATH/bin` 在你的 `PATH` 中。
:::

## Docker 镜像

如果上面的安装方式不支持你的环境，你可以选择 Kusion 镜像作为替代。

首先，拉取最新镜像：

```bash
docker pull kusionstack/kusion:latest
```

接下来，以交互式方式启动 Kusion 镜像：

```bash
docker run --rm -it kusionstack/kusion:latest bash
```
