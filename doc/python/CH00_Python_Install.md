# Python安装指南
Mac不再自带Python，需要自行前往官网下载，并安装，安装后运行Python Launch，注意程序名为`python3`
## 虚拟环境

虚拟环境创建了一个本环境专用的python隔离区：
1. 膨胀系统公共Python运行包库：包之间存在依赖关系，经常出现不可用的情况，各个项目需要的包大多不一致，很难One Track管理
2. 提供一套稳定的可运行包组合

用于创建虚拟环境有多种方式，如：
1. Anaconda：自动分析包依赖关系，
2. mini-conda：轻量级Anaconda，常用于python库的持续构建，避免重复下包
3. venv：Python内置虚拟环境，结合pip使用。

本文将基于venv进行虚拟环境的创建及管理：
```[bash]
# 创建
$ python -m venv venv

# 激活
$ source venv/bin/activate

# 此时python3已经为venv的python3
(venv) $ which python3
/<path_to_venv>/venv/bin/python3

# 该环境下使用到的包固化
(venv) $ pip freeze > requirements.txt

```

