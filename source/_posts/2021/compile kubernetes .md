layout: "post"
title: "compile kubernetes "
date: "2021-02-14 23:09"
tag:"k8s"
---
### 过程
```
make 
```


### problem
#### make error `Can't find 'go' in PATH, please fix and retry.`
```
cd kubernetes
sudo make
```
原因是，如果不适用sudo make 会提示用户没有权限创建目录。当使用sudo make时，切换至root权限，root权限没有配置go环境。检查方法如下：
```
# 对比二者差异
printenv
sudo printenv
```
#### 解决方法
```
sudo visudo
```
```
Defaults secure_path="$YOUR_GO_BIN_DIR:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
```

###  参考：[Run Local Kubernetes Cluster, Change Source Code, and Test](https://dzone.com/articles/easy-step-by-step-local-kubernetes-source-code-cha)
