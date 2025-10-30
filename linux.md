# 环境变量
.bashrc：日常命令及命令行配置  
.bash_profile：登陆时调用，放初始化配置（并调用.bashrc）  

## 添加新的环境变量
export PATH=$PATH:*/new/path*

# 密钥
1. ssh-keygen -t ed25519 -C *"note"*
2. copy *public_key* to remote *.ssh/authorized_keys*
3. sudo chmod 700 *path/.ssh*
4. sudo chmod 600 *path/.ssh/authorized_keys*
