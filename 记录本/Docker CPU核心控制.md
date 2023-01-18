
除了上述对CPU的使用限制外，现代的计算机一般是多核CPU，因此，我们有时还希望一个Docker容器能够固定在一个CPU上运行。这对于NUMA（即非一致存储访问结构）的服务器尤为有用，而对于简单的单核服务器则没有任何作用。
在Docker容器运行时，我们可以使用参数–cpuset来绑定CPU，使得该Docker容器只在固定的CPU上运行。
在Docker容器运行后，我们可以使用task命令查看Docker容器使用的CPU内核，如下所示：
![[dockerCPU核心限制命令.png]]
```bash
docker run -it --cpuset-cpus 8 centos /bin/bash
```

官方命令说明：
![[docker的cpu相关参数.png]]


[[技术]] [[docker]]   [[cpu核绑定]]
标签： #技术/docker/cpu性能  