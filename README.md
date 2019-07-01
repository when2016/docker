# docker
PS C:\Users\whe> mysql -uroot -h 188.131.169.24 --port=13306 -p
PS C:\Users\whe> redis-cli -h 188.131.169.24 -p 16379

























1.命令行登录到阿里云的doker仓库，--username为阿里云的用户名
sudo docker login --username=xxx registry.cn-qingdao.aliyuncs.com
2.创建命名空间wanghongen

3.查看要上传的镜像列表
[root@VM_0_6_centos ~]# docker images
REPOSITORY               TAG                 IMAGE ID            CREATED             SIZE
longmao/centos-mariadb   v1                  91be572f5d99        51 minutes ago      484 MB
docker.io/nginx          latest              719cd2e3ed04        2 weeks ago         109 MB
docker.io/centos         7.4.1708            9f266d35e02c        3 months ago        197 MB

4.为本地镜像添加tag
docker tag 91be572f5d99 registry.cn-qingdao.aliyuncs.com/wanghongen/centos-mariadb:v1

5.push到docker仓库
docker push registry.cn-qingdao.aliyuncs.com/wanghongen/centos-mariadb:v1