# Mojo-Webqq v2.1.4
使用Perl语言编写的Smartqq客户端框架，基于Mojolicious，要求Perl版本5.10+，可通过插件提供基于HTTP协议的api接口供其他语言或系统调用
</br>项目来源[Mojo-Webqq](https://github.com/sjdy521/Mojo-Webqq)，在此基础上添加IRC依赖模块，pl脚本添加IRCShell插件。 
</br>
#### 流程图

```

    +-------------------+                      +----------------+  
    |  Tencent          |                      | Any IRC Client |
    |  SmartQQ Server   |                      | wechat、irssi  |
    +---v-------------^-+                      +-v------------^-+     
        |             |                          |            |
        | QQ协议交互  |                          |IRC协议交互 |
+-- --- |--  - -  --  | - - -   --   -  -   ---  | ---  ----- | --+
|   +---v-------------^--+                  +----v------------^-+ |   
|   |                    <——————————————————<                   | |
|   |   SmartQQ Client   |     QQ - IRC     |  IRC Server       | |
|   |                    |     协议转换     |  监听本机6667端口 | |
|   |                    >——————————————————>                   | | 
|   +--------------------+                  +-------------------+ |
|                                                                 |
|                                       我们程序实现的部分        | 
+---  - - - -  -- - --  ----  ------  -------  ------  ---    ----+

```
### SmartQQ Client
Smartqq客户端只需双击此项目中start_mojo_webqq.bat或者start_mojo_weixin.bat批处理即可启动一个客户端。
![image](https://github.com/ghuan/springmvc/blob/master/WebContent/images/1.png)
### IRC Client
[IRC Client download](http://www.ircreviews.org/clients/) 请自行选择对应操作系统下载。
</br>
我使用的是irssi，windows操作系统下载cygwin</br>
![image](https://github.com/ghuan/springmvc/blob/master/WebContent/images/2.png)</br>
安装时加载irssi package。</br>
![image](https://github.com/ghuan/springmvc/blob/master/WebContent/images/3.png)</br>
### 建立IRC服务端
启动cygwin 键入命令 irssi -c 127.0.0.1 -p 6667</br>
IRC客户端常用操作命令

/nick 你的QQ昵称               #设置irc的昵称，建议和自己的QQ昵称相同</br>
/list -yes                    #列出自己加入的QQ群</br>
/query 对方qq昵称或群名称       #建立一个一对一私聊窗口</br>
[更多IRC命令](http://wiki.ubuntu.org.cn/IRC%E5%9F%BA%E6%9C%AC%E5%91%BD%E4%BB%A4%E8%AF%B4%E6%98%8E)</br>

### 效果图

![image](https://github.com/ghuan/springmvc/blob/master/WebContent/images/4.png)</br>
