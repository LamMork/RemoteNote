# Docker 指令大全

## **目录**
### 容器管理
- [run](#run)
- [start/stop/restart](#start)
### 容器操作
- [ps](#ps)
### 远程镜像仓库操作
- [login](#login)
- [pull](#pull)
- [push](#push)
- [search](#search)
### 本地镜像仓库操作
- [build](#build)


<span id="run"></span>

## **run**
使用指定的镜像，创建一个新的容器，并运行指定的指令
### 语法
> docker run [选项] 镜像 [指令] [args]
### 选项
- -i    &emsp;: 以交互模式运行容器（通常与 -t 共同使用）
- -t    &emsp;: 为容器重新分配一个伪输入终端（通常与 -i 共同使用）
- -rm   &emsp;: exit退出的时候自动删除创建的容器
### 实例
以 ubuntu15.10 镜像，创建一个新容器，然后在容器里面执行 echo。
```
$ docker run ubuntu:15.10 echo "Hello, world."
```
以 ubuntu14.04 镜像，建立一个新的交互式容器，并分配一个伪输入终端，设置退出终端的时候自动删除创建的容器
```
docker run -it -rm ubuntu:14.04 bash
```


<span id="ps"></span>

## **ps**
列出当前存在的容器
### 语法
> docker ps [选项]
### 实例
```
$ docker ps
```


<span id="start"></span>

## **start / stop / restart**
