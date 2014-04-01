mmonitor
========

+ 项目: mMonitor v1.0.1
+ 作者: Actrace(Coder) && Mille(Designer)
+ 更新: 2013-11-26
+ 版本: 2
+ 版权: GPL v3
+ 主页: http://mmonitor.org

简介
========

mMonitor是一款以PHP为语言编写的服务器监控软件.
总共包含监控器和探针两部分.
目前探针是针对centos服务器环境进行编写的,所以我们仅对centos系统进行了测试.
如果您需要安装到其他类unix系统上,请您测试探针是否能正常工作.

安装
========

+ 监控器部分.

    将本目录下所有文件上传至服务器后,你可以通过浏览器访问,引导程序会自行检查程序
    运行所需的环境组件,如果您的服务器缺乏环境组件,请按照提示修复.

    特殊:监控器包含了一个CLI模式下运行的信息收集程序(deamon.php),在web安装页面检
    查完毕后,您需要将该程序添加至系统计划任务中才能让程序正常工作.请添加计划任务
    每隔一分钟执行一次deamon.php.

+ 探针(get.php).
    
    直接将PHP探针上传到需要监控的服务器,一般支持PHP的普通web环境即可.

注意:deamon.php需要PCNTL库支持(CLI模式下).

使用
========

+ 用户管理,编辑 "data/userlist.php".

+ 增加,编辑,删除监控对象.

  初次安装的时候,在include目录里会有一个server文件夹,这是一个用于创建监控对象
的模板,将该文件夹复制到data目录里,然后进入该文件夹,编辑config.php即可.
