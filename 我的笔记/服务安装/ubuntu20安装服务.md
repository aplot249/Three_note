# ubuntu20安装服务
**安装 golang >= 1.16 和 nodejs >= 14.x**
--------------------------------------

1.  `wget https://deb.nodesource.com/setup_16.x` 数字16可以更改为其他版本号
2.  `bash setup_16.x && apt update && apt install nodejs -y` 进行安装
3.  `add-apt-repository ppa:longsleep/golang-backports` 添加go的ppa源
4.  `apt install golang-go -y`

**go另外安装教程**  
  
`* 进入网站  https://golang.google.cn/dl/ ，找到go语言安装包`  
``* 在ubuntu上执行 ` wget https://golang.google.cn/dl/go1.18.1.linux-amd64.tar.gz ` 拉去安装包``  
`` * 对安装包进行解压 ` tar -xzvf go1.18.1.linux-amd64.tar.gz` ``  
`` * 解压后复制 `mv go /usr/local/` ``  
`* 修改.bashrc文件 vim bashrc`  
    `export GOROOT=/usr/local/go              # 安装目录。`  
    `export GOPATH=$HOME/go     # 工作环境`  
    `export GOBIN=$GOPATH/bin           # 可执行文件存放`  
    `export PATH=$GOPATH:$GOBIN:$GOROOT/bin:$PATH       # 添加PATH路径`

`配置生效 source .bashrc`

**卸载 nodejs**
-------------

1.  `apt remove nodejs` 只会卸载 nodejs，但是会保留配置文件，方便以后再次安装 nodejs
2.  `apt purge nodejs` 如果不想保留配置文件，这将会卸载 nodejs 和其相关的配置文件。
3.  `apt autoremove` 移除和 nodejs 一起安装但是现在没有被使用的包

**安装certbot**
-------------

1.  pip3 install certbot

**安装mariadb**

1.  `安装 apt install mariadb-server`
2.  `重启一下 service mysql restart`
3.  `mysql_secure_installation`
4.  `更改登录方式`  
    `UPDATE mysql.user SET authentication_string = PASSWORD('mypassword'), plugin = 'mysql_native_password' WHERE User = 'root' AND Host = 'localhost';`
5.  `刷新权限 flush privileges;`
6.  `退出重新登录`
7.  `创建数据库 create database if not exists 数据库名 charset utf8 collate utf8_general_ci;`

### **解决MariaDB无密码 可登录**

`官方对此的解释为：`[`https://mariadb.com/kb/en/library/authentication-plugin-unix-socket/`](https://mariadb.com/kb/en/library/authentication-plugin-unix-socket/)  
`即通过系统认出是root直接认证，但是如果想换成必须用密码就需要改了这个模式`

`查看当前的认证状态：`  
`select user, plugin from user;`  
`结果如果为 unix_socket 就需要修改模式`  
`按照官网的说明修改就行`  
`ALTER USER root@localhost IDENTIFIED VIA mysql_native_password;`  
`这样可以修改模式为 mysql_native_password`

`查看修改后的状态：`  
`修改成功后发现还是可以通过mysql 或者mysql -uroot命令直接登录`  
`这里的坑就是，需要重新设置一下密码。即使你是从 mysql_native_password 模式变为mysql_native_password模式，也需要设置一下`

`重设密码：`  
`ALTER USER root@localhost IDENTIFIED BY 'yourpassword';`  
`其中以上的 root 代表用户 localhost代表可访问的地址，根据自己的情况修改即可`

### **Mariadb 设置远程访问**

1.  `添加远程访问账户 GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'passwd';`
2.  `修改配置文件，将配置文件中bind-address = 127.0.0.1加# 注释掉，或者修改其绑定的ip地址。`
3.  `重启mysql程序`