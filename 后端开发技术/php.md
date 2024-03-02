# PHP基础

### 客户端与服务器端

客户端：用户所使用的平台，如电脑、手机等

服务器端：给客户端或用户提供使用的计算机，任何主机都可以当作服务器

区别：服务器没有显示屏、鼠标、键盘，专门提供为客户端提供服务，在线访问网页时，其实是访问了相应的服务器

静态网站：数据是固定的，本地插入的

动态网站：数据是可变的，会更新

### 计算机通信

- 人与计算机通信：

JavaScript、java、php、python...

- 计算机与计算机：

ip地址（当前主机的唯一标识）

查看自己本机的IP地址**window+R-->cmd-->ipconfig-->IPv4地址**

- 计算机通信过程

访问某网站

ip:192.168.xxx.xxx(0-255)

域名(ip的别名)：http://www.jd.com/

ip是唯一的，但域名可多个，域名对应一个ip，但ip可对多个域名

输入域名后访问过程：
1. www.jd.com --> 找**DNS服务器**进行域名解析成ip地址 --> 返回**客户端**浏览器
2. 拿到解析的ip地址后 --> 请求这个**ip地址的服务器**
3. 服务器接收请求
4. 服务器处理请求
5. 服务器响应处理
6. 浏览器**客户端**接收响应的数据
7. 页面渲染 ---dom --css --images --js

### 通信访问url

- 访问呢服务器时：
**https协议 + 域名 + 端口号**（网页的端口号：80/8080）

### 安装xampp

- php脚本语言 开源，可以访问服务器，对数据库增删改查（后台语言）

后台语言： php java c python

注意：php是操作服务器，不能在客户端直接运行，所以需要安装环境

安装的是集成环境 xampp工具：使本机运行php，让本机成为服务器

- 安装

### xampp启动文件
0. 启动xampp-control.exe文件，打开
1. 打开浏览器-在地址栏输入localhost（指本机的网址，会访问对应的（本机）服务器,改了端口号需要加上:8083等）
2. 找到根目录xampp/htdocs/ （装的本机服务器就在这里，里面的内容都删掉）
3. **htdocs根目录**就是放置项目文件的地方，即**本地的服务器**

**进入项目时，默认是index页面**

### php文件创建
1. 建立.php文件
2. 语法 

    输<?php

    输   php内容

    输?>

3. 注释： //单行注释 /**/多行注释  #注释
4. 输出语句  echo 'hello'; 
5. 可支持 HTML  echo '<h 2>标题<h 2>'

### 数据类型string
$变量名='hello';

$bianliang='hello'; #赋值是弱类型

echo $bianliang;

- js数据类型
string number boolean null **undefined** object
- php数据类型
string **Integer整数 float浮点** boolean null object
- php判断
echo gettype($bianliang); #string
- 字符串拼接
$str="hello world";

echo $str

echo "$str" #双引号会解析内容

echo 'hello world'#以上三个输出相同

echo '小明说:'.$str."我说$str" #用.拼接，最佳方法可都放双引号中

### 定义数组

### 数组遍历

### get请求传递参数

### form表单-预定义变量

### php和html嵌套

### 创建数据库

