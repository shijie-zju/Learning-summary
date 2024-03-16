# Chatglm6B

### 部署教程

https://www.bilibili.com/video/BV1K14y1m7Hu/?spm_id_from=333.788.top_right_bar_window_custom_collection.content.click&vd_source=c37728f2b9891208b9908ab937dbade2


1. 阿里云上创建DSW实例
2. 更新git-lfs(某插件，允许Git版本控制系统更有效地存储和管理大型文件，在终端进行):

apt-get update

apt-get install git-lfs

3. 初始化git设置

git init

git lfs install

4. 下载源代码
git clone https://github.com/THUDM/ChatGLM-6B.git

或下载压缩包，然后  unzip 路径名称  解压

5. 下载依赖

cd ChatGLM-6B

pip install -r requirements.txt

6. 下载模型

mkdir model

cd model

git clone https://huggingface.co/THUDM/chatglm-6b

更改demo中的路径，然后运行
