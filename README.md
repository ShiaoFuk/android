# android
## 软件功能
此软件仿照深圳大学内部网的网页风格打造，同时适用于android端平板和手机，实现了登录、内部网事务的基本功能，让学生可以在移动端办理内部网事务，只需要无线网络连接到内网即可。
## 环境
android studio导入，等待gradle下载完毕后build项目
## 使用说明
1. 登录
  因为没有内部网的数据库权限，自行模拟了登录，用java写的后端登录，通过发送账号密码到后端，后端验证完毕后发送令牌和expire time。
2. 使用
  内部网的内容只有主体一级网页部分，二级网页部分是通过调用移动端浏览器打开实现的。
## 代码目录架构
│  Communication.java // 自定义的网络库模板，用于发送get和post请求
│  MainActivity.java  // 主页面
│  Response.java  // response类用于存取响应信息，包括响应头、响应体
│  
├─Broadcast
│      OnlineBroadcastReceiver.java  // 广播类，断网时自动退出登录
│      
├─Cyper
│      GenerateKey.java  // 加密类，用rsa加密
│      
├─Login  // 登录相关
│      Login.java
│      LoginActivity.java
│      PasswordEditText.java  // 自定义组件，继承editext
│      Register.java
│      User.java
│      UserEditText.java  // 自定义组件，继承editext
│      
├─NewsItem
│      NewsItem.java
│      
├─SZUFragment  // 仿照网页，区分为左右两个fragment
│  ├─LeftFragment
│  │      ContentProvider.java
│  │      LeftFragment.java
│  │      
│  └─RightFragment
│          RightFragment.java
│          
└─Thread
        Callback.java
        Task.java
## 许可证
apache license
## 联系方式
mashufu@outlook.com

        
