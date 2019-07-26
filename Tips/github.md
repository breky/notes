## Record Git Error

**Table of Content**

- [常用命令](#commands)

- [Permission denied](#permission-Denied)

### Commands

1. 全局命令

   1.1 git --global user.name "user name"

   1.2 git --global user.email "user email"

2. ssh

    2.1 ssh-keygen -t rsa -b 4096 -C "user email"

    2.2 ssh-add ~/.ssh/id_rsa


3. 添加远程仓库

    3.1 git remote add notes address of remote repository

4. pull

    4.1 git pull notes master

5. push

    5.1 git add . and git status
 
    5.2 git commit -m "message"

    5.3 git push notes maser
 

### Permission Denied 

```shell
git@github.com: Permission denied (publickey)
```


1.  ssh-key 

    ssh-keygen -t rsa -b 4096 -C "email@xxx"

2. ssh -v git@github.com

    最后两句会出现：

    No more authentication methods to try.  

    Permission denied (publickey).

3. ssh-agent -s

    然后会提示类似的信息：

    SSH_AUTH_SOCK=/tmp/ssh-GTpABX1a05qH/agent.404; export SSH_AUTH_SOCK;  

    SSH_AGENT_PID=13144; export SSH_AGENT_PID;  

    echo Agent pid 13144;

4. ssh-add ~/.ssh/id_rsa(id_rsa 路径)

    这时候应该会提示：

    Identity added: ...（这里是一些ssh key文件路径的信息）
    (
    **注意:**

    如果出现错误提示：

　　Could not open a connection to your authentication agent.

　　请执行命令：
　　
　　eval `ssh-agent -s`
　　
　　后继续执行命令 ssh-add ~/.ssh/id_rsa

5. 将 id_rsa.pub 的内容添加到 Deploy key 中
