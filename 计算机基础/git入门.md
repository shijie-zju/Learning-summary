# git入门

## 新建git账号、邮箱及指定文件下建立git仓库

git config --global user.name songshijie

git config --global user.email 1724926804

git init  (指定文件夹下创建git仓库)

echo "版本时间23.1.5" > README.md（建个文件）


## 仓库资源的管理
**git status**（显示当前所处的分支）

git add README.md（加入文件至缓存区！）

git commit -m "版本时间24.1.5"（提交缓存区内容！）

**git commit -am "版本时间24.1.5"**（二合一:将所有修改的已跟踪文件加入到提交中）

**git log** （查看前面的更改版本）


## 主线与分支管理
touch .gitignore（创建ignore可以往里存放不想被git查看的文件名）
（往.gitignore中添加文件名就可以使被添加文件被忽略分支）

git branch fenzhi1（创建分支）

git branch （查看分支）

git checkout fenzhi1（切换分支，切换后会读取当前分支内容） 

git branch -d fenzhi1 （换为-D强制删除分支）

git merge fenzhi2（将其他分支合并至主分支master上）


## 远程仓库（如github）
**git clone** https://github.com/sun-team-zju/songshijie.git （远程克隆到本地）

**git remote add origin** https://github.com/shijie-zju/zjustudy.git (添加远程仓库)

**git push origin main:main -f**:如果不小心创建了分支，可以把它强制规定到主分支下！


**git remote -v**（查看本地和远程哪些仓库联系）

**git push** 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（更新至我的远程仓库中）

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

[视频教程：git工作流和核心原理  bilibili](https://www.bilibili.com/video/BV1r3411F7kn/?spm_id_from=333.1007.top_right_bar_window_default_collection.content.click&vd_source=c37728f2b9891208b9908ab937dbade2)
![Alt text](../pictures/FF05D60A6858400063834B9014BFAD71.jpg)


创建一个团队项目总结：
![Alt text](../pictures/gitteam.png)

1. **单次；新建本地git:** 本地创建项目文件夹，右键git bash

git config --global user.name songshijie

git config --global user.email 1724926804

git init  (指定文件夹下创建git仓库)

2. **反复：编辑更新至本地git:** 本地编辑结束后进行

git add 待添加的文件名（或git add . 添加当前目录全部文件）

方式1： git commit (将所有的add的保存为一个版本)
->进入vim编辑器进行版本命名：
按a/i 进入编辑模型，编辑，按esc退出编辑，:wq保存退出

方式2： git commit -m "3/1/fix(修复模块)：修复的内容说明"

git log （查看提交的日志）

回退至某版本：git log 查看版本，复制要回退的版本id,然后输入：

git reset --hard 版本号

3. **单次：将本地git与远程新建仓库绑定并上传内容:** 本地进行操作

git branch -M main （创建一个main分支，并将主分支切换为main）

git remote add origin https://github.com/shijie-zju/langchain-web.git（添加远程仓库地址）

git push （推送上传至远程仓库）

4. **参与开源项目：** 别人右上角fork至自己的远程仓库，返回自己仓库找到clone地址，返回本地新的文件下，然后

git clone 地址名 . 

git remote -v （查看本地绑定的仓库链接）

git remote add upstream 上游仓库的链接 （这里upstream指开源的仓库）

git checkout -b fenzhi1 （创建并切换至新分支）

在本地就可以参与项目更改了，修改完成后add commit git push -u origin 
自己的远程仓库就多了个分支

这时来到开源项目下，pull requests进入，选择head为对方main分支，compare选自己的分支。如果是对勾则可以pull request提交自己的分支

若不是绿色对勾：
git merge upstream/main （将远程upstream的main分支merge合并至目前的本地分支上），改完后再执行git push更新自己的远程仓库

<div style="text-align: right;">

[返回主页](../README.md)
</div>