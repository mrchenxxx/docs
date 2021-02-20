## 在 ``cenos`` 上安装
> [!TIP|label:步骤]
> 1. 卸载旧版本
> ``` linux
> sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
    ```
> 2. 设置Docker存储库
> ``` linux
> sudo yum install -y yum-utils
    ```
> ``` linux
> sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
    ```
> 3. 安装DOCKER
> ``` linux
> sudo yum install docker-ce docker-ce-cli containerd.io
> ```


## docker 配置阿里云镜像加速
> [!TIP|label:步骤]
> 1. 打开 [阿里云](https://cr.console.aliyun.com/cn-hangzhou/instances/mirrors) （控制台 → 左上角菜单 → 产品与服务 → 弹性计算 → 容器镜像服务 → 镜像加速器）
> 其中涉及到 设置密码等操作 这里就不再赘述    
> 
> 2. 按照下图所示步骤即可完成 阿里云镜像加速
> 
> ![加速](../../_media/docker/阿里云镜像加速.png)

> [!WARNING|label:注意]
> 配置阿里云镜像加速时要看自己的操作系统是啥，我是在树莓派上部署的用的是乌班图，如果在阿里云主机上用centos系统 就按照centos系统的指示来

## docker run的原理和流程
> [!TIP|label:如图所示]
> ![原理图](../../_media/docker/run的流程图.png)

## mysql

### 安装
> [!TIP|label:步骤]
> 1. 输入指令：
> ``docker pull hypriot/rpi-mysql:latest``
> 
> 2. run:
> ``docker run --name mysql -e MYSQL_ROOT_PASSWORD=123456 -d -p 3306:3306 hypriot/rpi-mysql``



