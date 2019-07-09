## Linux 常用命令

### 添加环境变量

XXX_HOME=xxx_path
export PATH=$XXX_HOME:$PATH

### 解压 tar 包

tar -zxvf xxx.tar -C path

-z: 使用 gzip 解压文档
-x: extract, 解压
-v: verbose, 显示解压详细信息
-f: 

-C: 解压到 path 目录


### 打包 tar 包

tar -cf xxx.tar

-c: create, 创建一个新的 tar 包

