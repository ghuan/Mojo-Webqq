# Mojo-Webqq for windows
该项目是使用Perl语言编写的Smartqq客户端框架，基于Mojolicious，要求Perl版本5.10+，可通过插件提供基于HTTP协议的api接口供其他语言或系统调用
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
