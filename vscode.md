### vscode使用推荐
> `轻便`，`颜值即正义`, `速度快`，`插件安装方便`，`直连服务器`......

- 配置文件
> vscode中的配置分用户区（User）和工作区（Workspace）。   
> 覆盖范围：用户区 > 工作区  
> 优先级：工作区 > 用户区

#### 插件推荐
> 编程语言相关插件就不说了，直接按照官方推荐来就好了。

- Remote Development
> 一个远程连接工具包，目前只用到了里面的`remote-ssh`，用于连接服务器。  
> 可以直接将服务器上一切在本地vscode中使用，简直不要太爽！！！

**连接方式**  
左侧点击插件->点击齿轮->修改配置信息
```
Host 随便取个名
    HostName [主机ip]
    User [用户名]
    IdentityFile [如果设置了ssh密钥登陆，这里填写密钥地址，否则，可以不用此项]
```
> **注意**: 连接成功后，会在服务器的用户根目录下创建一个`.vscode-server`文件夹，里面存放远端vscode配置信息。第一次连接或者vscode更新时，服务器需要连网。

- 配色和字体推荐  
> 配色推荐：Monokai Pro(直接在扩展中心安装即可)  
> 字体推荐：[FiraCode](https://github.com/tonsky/FiraCode) [[安装教程](https://github.com/tonsky/FiraCode/wiki)]

显示效果：  
![vscode配色效果](/images/vscode/fonts-theme.png)

- Settings Sync  
> 将vscode配置（包括插件）同步到github gist中，方便一键移植。
> [配置教程](https://juejin.im/post/5b9b5a6f6fb9a05d22728e36)
> 上传配置快捷键: shift+Alt/option+U
> 下载配置快捷键: shift+Alt/option+D

- 其他插件

|          插件         |           功能          |
|:---------------------:|:-----------------------:|
| Chinese Language Pack |       vscode汉化包      |
|      Code Runner      |     一键运行所有程序    |
|   Code Spell Checker  |     英文单词检查插件    |
|        Edit csv       |   csv文件可视化编辑器   |
|        filesize       | 在底部bar中显示文件大小 |
|  github pull requests |        集成github       |
|     LaTex Workshop    |        集成LaTex        |
|       Live Share      |       远程协同编程      |
|   Path Autocomplete   |     路径自动补全插件    |
|          Vim          |        vim快捷键        |
|        TabNine        |        AI补代码        |