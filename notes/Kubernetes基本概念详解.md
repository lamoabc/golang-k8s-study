# Kubernetes基本概念详解

----

## 1.Kubernetes组件

![img](https://cdn.nlark.com/yuque/0/2022/svg/22380443/1656509502594-fb6cebd0-239e-43d6-b59e-5093954f9957.svg)

## 2.Kubernetes中各组件

### 2.1 Control Plane Components(控制平面组件)

一般在kubernetes集群中部署在master节点上,起到控制管理全局的作用

#### kube-apiserver 

#### etcd 

#### kube-scheduler

#### kube-controller-manager

### 2.2 Node 组件 

#### kubelet

#### kube-proxy 

#### Container Runtime



## 3.Kubernetes中涉及到的基本概念

### Pod

### Deployments和ReplicaSet

### Service和Ingress

### Volume

### ConfigMap和Secret

### namespace



参考资料链接:

1. https://kubernetes.io/docs/concepts/
2. https://zhuanlan.zhihu.com/p/292081941