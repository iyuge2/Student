#### 使用ssh免密登录服务器

- 在服务器端使用`ssh-keygen`生成密钥对，在用户的家目录中生成了一个 .ssh 的隐藏目录，内含两个密钥文件，id_rsa 为私钥，id_rsa.pub 为公钥。
```
cd ~/.ssh
cat id_rsa.pub >> authorized_keys
chmod 600 authorized_keys
chmod 700 ~/.ssh
```

- 设置 SSH，打开密钥登录功能，编辑 /etc/ssh/sshd_config 文件，进行如下设置：
```
RSAAuthentication yes
PubkeyAuthentication yes
```

- 重启ssh服务
```
/etc/init.d/ssh restart
```

- 在本地~/.ssh/目录下新建一个文件（名字随便取）,将服务器端的私钥id_rsa里的全部内容复制到新建的文件中，并将该文件权限改为`0600`
> 注意，windows用户“~”目录一般为`C:\Users\***`

- 本地使用下面命令进行登陆
```
ssh xxx@xxx.xxx.xxx.xxx -p [端口号] -i ~/.ssh/[filename]
```

- 设置别称，方便下次登录，在用户配置文件中用`alias`给上述命令取一个别称。
```
vim ~/.bashrc
alias xxx = 'ssh xxx@xxx.xxx.xxx.xxx -p [端口号] -i ~/.ssh/[filename]'
```