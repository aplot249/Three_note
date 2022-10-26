# 腾讯云ubuntu开启root登录
| 步骤  | 方法  |
| --- | --- |
| 修改 root 密码 | 执行命令sudo passwd root |
| 输入密码 | 可以和 ubuntu 密码一致，也可以修改 (密码会让你输入两次) |
| 修改 ssh 配置 | 执行命令sudo vi /etc/ssh/sshd\_config |
| 修改  | PermitRootLogin |
| 重启 ssh 服务 | 执行命令sudo service ssh restart |