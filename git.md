# 基础设置
- git config --global user.name "*your_name*"
- git config --global user.email *email_address@email.com*
- git config --global core.editor vim
- git config --global init.defaultBranch *main*
- git config --global color.ui auto
## 查看配置情况
- git config --list

# 连接远程github
## SSH配置
1. ssh-keygen -t rsa
2. 将公钥填写到github上
## 测试SSH配置
ssh -T git@github.com
## 配置SSH端口和代理
>22端口（SSH默认端口）被屏蔽时，可以改用443端口<br>
>.ssh文件夹中添加config文件<br>
>注意修改私钥地址<br>
>代理中-V可选，代理端口注意修改<br>
```
Host github.com
  HostName ssh.github.com
  User git
  Port 443
  IdentityFile ~/.ssh/id_rsa
  ProxyCommand nc -V -x 127.0.0.1:7890 %h %p
````

# 重命名本地Git分支
## 查看本地分支
git branch -a
## 切换到需要重命名的分支
git checkout *branch_name*
## 重命名
git branch -m *new_name*

# 推送本地仓库到远程仓库
## 初始化本地仓库
git init
## 追踪本地文件
git add *files you need*
## 添加评论
git commit -m "*comments*"
## 添加远程仓库地址
git remote add origin *repository_address*
## 推送
git push -u origin *branch_name*

# 从远程仓库拉取
## 添加远程地址
git remote add origin *repository_address*
## 拉取内容
git pull origin *branch_name*
## 修改/删除远程仓库地址
git remote rename origin *repository_address*<br>
git remote remove origin
## 查看远程仓库链接
git remote -v

# .gitignore
## 基础
- !忽略匹配到的文件/文件夹
- #注释
- ?任意一个字符
- [abc]匹配abc中的任意字符
