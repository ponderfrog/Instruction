# 基础设置
- git config --global user.name *"your_name"*
- git config --global user.email *email_address@email.com*
- git config --global core.editor vim
- git config --global init.defaultBranch *main*
- git config --global color.ui auto

# 查看配置情况
- git config --list

# 连接远程github
## SSH配置
1. ssh-keygen -t rsa
2. 将公钥填写到github上
## 测试SSH配置
ssh -T git@github.com

# 重命名本地Git分支
## 查看本地分支
git branch -a
## 切换到需要重命名的分支
git checkout *branch_name*
## 重命名
git branch -m *new_name*

