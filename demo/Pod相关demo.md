# Pod 相关demo

---

## 1.为容器的生命周期时间设置处理函数

官方文档地址 : [https://kubernetes.io/zh-cn/docs/tasks/configure-pod-container/attach-handler-lifecycle-event/](https://kubernetes.io/zh-cn/docs/tasks/configure-pod-container/attach-handler-lifecycle-event/)

### 1.1.基础环境

- 搭建 Kubernetes 集群
- 安装 `kubectl` 工具

### 1.2.定义 postStart 和 preStop 处理函数

``` yaml
apiVersion: v1

kind: Pod

metadata:

  name: lifecycle-demo

spec:

  containers:

  - name: lifecycle-demo-container

    image: nginx

    lifecycle:

      postStart:

        exec:

          command: ["/bin/sh", "-c", "echo Hello from the postStart handler > /usr/share/message"]

      preStop:

        exec:

          command: ["/bin/sh","-c","nginx -s quit; while killall -0 nginx; do sleep 1; done"]
```



### 1.3.具体操作

1. 应用yaml

   >![img](.\img\create lifecycle yaml.png)
   >
   >
   >
   >切记
   >
   >1. 机器内存要够
   >2. 确保集群所有节点能正确运行

   

2. 





## 2.配置存活、就绪和启动探测器

官方文档地址 : [https://kubernetes.io/zh-cn/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/](https://kubernetes.io/zh-cn/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/)