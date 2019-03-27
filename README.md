# Go Language for Raspberry PI3

这是针对树莓派3b的 Go 语言 Docker 运行容器镜像，相对「半官方」的 [Go 运行镜像](https://hub.docker.com/r/arm32v7/golang)这个镜像优化又以下几个优化点：

1. 基于 alpine 以及 go 的最新版本编译，比较轻量；
2. 使用 [resin 提供优化的 go 编译包](https://github.com/balena-io-library/base-images)；
3. 针对中国环境，apline 这块使用国内清华源镜像。

## 编译和运行镜像

使用 docker-compose 能够简化编译的过程，使用 `docker-compose build` 即可实现 Docker 镜像的编译。然后，运行 `docker run --rm raspberry-pi3-golang` 默认就可以打印镜像中 Go 的版本。

例如，以下镜像就可以正常使用了：

```
$ docker run --rm raspberry-pi3-golang
go version go1.12.1 linux/arm
```

Have fun :^9