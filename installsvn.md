# 安装svn
yum install subversion

# 创建svn仓库
* mkdir /data/svn
* svnadmin create /data/svn/ox

# 配置svn
* cd /data/svn/ox/conf
* vi svnserve.conf
* 设置选项 
    * anon-access = none
    * password-db = passwd

# 启动svn
svnserve -d -r /data/svn

# svn checkout
svn checkout svn://127.0.0.0.1/ox
