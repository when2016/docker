
参考
https://www.cnblogs.com/lemon-le/p/9914820.html
https://www.jianshu.com/p/ac87ae10f03f

https://www.cnblogs.com/lemon-le/p/9914820.html
https://www.jianshu.com/p/ac87ae10f03f


systemctl start etcd                          master
systemctl start docker                        node  
systemctl start kube-apiserver                master
systemctl start kube-controller-manager       master
systemctl start kube-scheduler                master
systemctl start kubelet                       node
systemctl start kube-proxy                    node



###1-2.将mysql-controller发布到Kubernetes集群中
kubectl create -f mysql-rc.yaml
###1-2.查看刚刚创建的RC
kubectl get rc
kubectl describe pod mysql

###2-1.创建Service对象
kubectl create -f mysql-svc.yaml
###2-2.查看刚刚创建的service
kubectl get svc

###3-1.将tomcat发布到Kubernetes集群中 
kubectl create -f myweb-rc.yaml
###3-2.创建对应的Kubernetes Service 
kubectl create -f myweb-svc.yaml 
###4.外网网络不通，无法访问，解决文案
iptables -P FORWARD ACCEPT


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