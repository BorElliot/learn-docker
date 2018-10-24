# gogs安装步骤

docker pull gogs/gogs

mkdir -p /var/gogs

docker run --name=gogs-data --entrypoint /bin/true gogs/gogs

docker run -d --name=gogs --volumes-from gogs-data -p 10022:22 -p 10080:3000 gogs/gogs

参考

[https://github.com/gogs/gogs/tree/master/docker](https://github.com/gogs/gogs/tree/master/docker)