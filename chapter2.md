# Docker的常用操作

## 查看信息
docker info

## 查看版本
docker --version

## 删除不再使用的容器实例
docker rm $(docker ps -aq)

## 删除镜像
docker rmi $(docker images -q)

## 查看容器实例
docker container ls

## 查看镜像
docker images

## docker run指令
用于通过镜像运行容器, 示例: docker run -it --rm --name go-instance -p 8080:8080 -v /host_dir:/container_dir golang

+ -it 用于交互模式启动并进入容器
+ --rm 用于在容器关闭后自动清理其中的内容
+ --name 将实例命名为
+ -p 容器端口和宿主的映射
+ -v 使容器可访问宿主文件 <host_dir>:<container_dir>