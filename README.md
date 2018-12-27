# learn-php

部署php项目大概流程：在本地用GitBash创建Lumen项目，写好代码，然后用Sublime的SFTP传到服务器，或者push到coding，然后在服务器pull下来。pull下来后用composer安装相关库

安装必要的库 conposer i | install

升级 PHP到7.2
yum remove php
rp -e [...依赖]

sudo rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
sudo rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm
yum install yum install  php72w-cli.x86_64 php72w-common.x86_64 php72w-gd.x86_64 php72w-ldap.x86_64 php72w-mbstring.x86_64 php72w-mcrypt.x86_64 php72w-mysql.x86_64 php72w-pdo.x86_64

yum install php72w-fpm

systemctl enable php-fpm

添加环境变量：PATH=$PATH:[可执行文件的路径]
生效环境变量 source /etc/profile

新建文件 ：touch 文件名

全局安装composer--前提是能执行php命令

curl -sS https://getcomposer.org/installer | php
mv composer.phar [/usr/bin/composer] 具体看自己的系统，因为我系统可执行文件放这里。

查看安装的php扩展：php -m 
