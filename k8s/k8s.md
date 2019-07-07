
参考
https://blog.csdn.net/hahachenchen789/article/details/80619590
https://www.cnblogs.com/niechen/p/10359711.html


###1.创建RC
kubectl create -f tomcat-rc.yaml
###2.查看RC
kubectl get rc

###3.创建服务Service
kubectl create -f tomcat-svc.yaml
###4.查看服务Service
kubectl get svc

###5.查看Pod的创建情况
kubectl get pods