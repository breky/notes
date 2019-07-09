## Record Git Error

Table of Content


-[git@github.com: Permission denied (publickey)](#git@github.com: Permission denied (publickey))


### git@github.com: Permission denied (publickey)

1. 创建 ssh-key 

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
    
    **注意:**

    如果出现错误提示：

　　Could not open a connection to your authentication agent.

　　请执行命令：

    eval `ssh-agent -s`

    后继续执行命令 ssh-add ~/.ssh/id_rsa

5. 将 id_rsa.pub 的内容添加到 Deploy key 中
