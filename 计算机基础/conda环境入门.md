# conda环境入门

## 下载
打开pytorch官网，确定runtime版本 选新的12.1<12.3 √

conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia

或者：
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
![Alt text](../pictures/QQ%E5%9B%BE%E7%89%8720240109144637.png)

## 创建虚拟环境

conda env list 查看已有的环境
![Alt text](../pictures/QQ%E5%9B%BE%E7%89%8720240109144630.png)

## 在某环境下下载相关库

conda activate torchgpu 进入某环境下

conda list 查看已安装的库

pip list

pip install numpy 安装某个库（推荐使用pip）