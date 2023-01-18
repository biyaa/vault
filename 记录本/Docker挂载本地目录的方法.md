docker可以支持把一个宿主机上的目录挂载到镜像里。
```bash
docker run -it -v /home/dock/downloads:/usr/downloads ubuntu64 /bin/bash

```

通过-v参数，冒号前为宿主机目录，必须为绝对路径，冒号后为镜像内挂载的路径。

[[docker]] [[挂载本地文件夹]]

标签： #技术/docker/挂载本地目录