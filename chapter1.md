## 在Centos 7安装docker

1. yum install -y yum-utils

2. wget http://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && rpm -ivh epel-release-latest-7.noarch.rpm

3. yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

4. yum -y --enablerepo=rhui-REGION-rhel-server-extras install container-selinux

5. yum install -y docker-ce

6. docker --version

7. systemctl restart docker

8. systemctl enable docker

9. 测试 docker run --name webserver -d -p 9090:80 nginx

10. 安装完成后，需要把当前用户添加到用户组才能不以root身份运行 sudo usermod -aG docker ec2-user