
##参考https://idc.wanyunshuju.com/Dr/603.html

##3.创建镜像
[root@VM_0_6_centos mariadb_dockerfile]# docker build -t longmao/centos-mariadb:v1 ./
##4.创建容器
[root@VM_0_6_centos mariadb_dockerfile]# docker run -d -p 13306:3306 longmao/centos-mariadb:v1 /root/run.sh
bed2afb5ad78120a4ce2efbde612ec2b73bcffaefa65735275f17b1d89fd9a37
##5.登录验证
PS C:\Users\whe> mysql -uroot -h 188.131.169.24 --port=13306 -p
Enter password: ******
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 4
Server version: 5.5.60-MariaDB MariaDB Server

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

