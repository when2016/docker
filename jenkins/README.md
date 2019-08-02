##1.安装docker
curl -fsSL https://get.docker.com | bash -s docker --mirror Aliyun
##2.安装jenkins https://www.cnblogs.com/stulzq/p/8627360.html
https://www.cnblogs.com/stulzq/p/8627360.html


###docker下安装jenkins步骤
1.

3.构建image
docker build . -t auto-jenkins
4.在启动Jenkins时，需要先创建一个Jenkins的配置目录，并且挂载到docker 里的Jenkins目录
mkdir -p /var/jenkins_home
5.修改目录权限（很重要！）
chown -R 1000 /var/jenkins_home
6.运行 Jenkins
docker run --name jenkins -p 8080:8080 -p 50000:50000 \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -v $(which docker):/bin/docker \
    -v /var/jenkins_home:/var/jenkins_home \
    -d auto-jenkins
7.通过ip:port访问jenkins
http://47.104.91.236:8080/
8.查看登录密码
cat /var/jenkins_home/secrets/initialAdminPassword


[root@l-maven-server1 wang]# cat readme.txt

java -jar -Dserver.port=18080 longmao-server-task-1.0.jar --spring.profiles.active=test

nohup java -jar -Dserver.port=18080 longmao-server-task-1.0.jar --spring.profiles.active=test > nohup.out &
