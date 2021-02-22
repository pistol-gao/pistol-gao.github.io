layout: "post"
title: "本地编译启动k8s"
date: "2021-02-21 14:35"
---

## 本地启动Kubernetes
```
$ sudo make clean
$ sudo make
$ sudo PATH=$PATH hack/local-up-cluster.sh
```
## kubectl配置
```
export KUBECONFIG=/var/run/kubernetes/admin.kubeconfig
```

## 检查本地集群状态
```
cluster/kubectl.sh cluster-info
```

## ectd查看
```
# 运行此命令需要将$GOPATH/src/k8s.io/kubernetes/third_party/etcd设置为PATH
etcdctl get --prefix / #可以查看到已经插入了很多k8s数据
```

## 参考资料
https://developer.ibm.com/components/kubernetes/articles/setup-guide-for-kubernetes-developers/
