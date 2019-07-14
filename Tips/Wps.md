## WPS 缺失字体

WPS Linux 版本安装完成后，打开时提示字体缺失，这篇文章记录此问题处理方法。

操作系统：Ubuntu 18.04 LST

WPS 版本：WPS Office 2019

### 下载字体

链接: https://pan.baidu.com/s/1yFg7nRafcdPYtnHJk38r1g 密码: 3xqf

### 安装字体

首先，将字体复制到 /usr/share/fonts 文件夹；

```shell
sudo cp * /usr/share/fonts # 在下载文件解压后的目录中
```

然后，从终端进入 /usr/share/fonts 文件夹下，执行以下代码;

```shell
sudo mkfontdir
sudo mkfontscale
sudo fc-cache
```

最后，重启 WPS。

### 参考文献

- [linux 系统安装WPS启动后报系统缺失字体](https://blog.csdn.net/dejunyang/article/details/81437632)

- [wps安装完成后提示系统缺失字体的解决方法](https://blog.csdn.net/sailor201211/article/details/23490099)

- [Ubuntu 16.04 LTS 字体路径](https://blog.csdn.net/yilovexing/article/details/80242722)
