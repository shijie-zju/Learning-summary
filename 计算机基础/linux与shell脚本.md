# linux

ls 列出当前目录所有文件 （-l所有属性：drwxr-xr--; -a 隐藏文件）

ll 列出所有信息

cd 进入一个目录 （.. 上一个目录; - 上次位置）

pwd 打印当前路径

cat 文件 查看当前的文件 （head 只看开头 head --lines=3 只看前三行）

less/more 文件 查看当前文件 （q退出）

mv 原名 新名  改文件名

#### 文件编辑器： nano, vim

nano 文件 进入编辑器可编辑文件（ctrl x 退出 ctrl o 保存）

vim 文件  进入编辑器可编辑文件 （i 插入模式 esc 退出模式 :wq保存退出  :q!强制退出）

file 文件  查看文件的类型格式

where/which gcc 查找应用程序位置 

#### echo、变量和for

h="hello"

echo $h 打印某内容,变量使用要加$

echo "i say $h"

for ff in week??  遍历以week开头后面有两个字符的文件

for ff in week* 以week开头的文件

for> do  执行

for> echo $ff week${ff#chapter} 打印：ff变量+week+ff变量中去掉chapter的内容

for> done 结束

#掐头 %去尾 + 掐去的内容



