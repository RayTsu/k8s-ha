# k8s-ha
# 注意！
* 1

```css
如果在节点执行kubectl get csr报错，那么在安装脚本执行完毕后执行将master节点上的~./kube/config 文件拷贝至各节点的/etc/kubernetes/下面，并重命名为并重命名为kubelet.kubeconfig
```
* 2

```css
vip最好选取实际存在的同网段地址，端口依旧设置成6443
```

* 3

```css
当启动pod出现以下类似错误时：试着给proxy.j2配置中加上这两个配置"--masquerade-all=true --proxy-mode=ipvs"
错误：Error while initializing connection to Kubernetes apiserver. This most likely means that the cluster is misconfigured (e.g., it has invalid apiserver certificates or service accounts configuration) or the --apiserver-host param points to a server that does not exist. Reason: Get https://10.68.0.1:443/version: dial tcp 10.68.0.1:443: getsockopt: connection refused
```