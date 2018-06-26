**目录**

[TOC]

# MaterialAboutIceAndFire

course material about Ice and fire 

## Description

* [Exercise](./Exercise) 课程中练习文件，可以直接使用做练习，注意配合课程标题
* [Project_IceAndFire](./Project_IceAndFire) 课程中项目文件直接使用该文件做项目
* [environment.yaml](./environment.yaml) 该文件是课程中 `workspace` 的工作环境配置文件，可以直接使用该文件配置工作环境，创建工作环境命令：`conda env create -f environment.yaml`。具体详情参见 `Anaconda` 课程部分。



## 环境配置可行方案——不建议使用 `environment.yaml`

因为存在以上相关的报错信息，提出一个相对完善的解决方案，直接查询在课程课程中需要的 `package` 版本号，使用 `conda install ` 命令进行本地安装。步骤如下：

- 在 `workspace` 中输入命令查询相关 `package` 版本，例如查询 `pandas`——`!conda list | grep pandas`

  ![](https://user-images.githubusercontent.com/24636410/41892456-b6f4bcd0-794a-11e8-9137-3ffcaa938068.png)

- 在本地运行安装命令并指定版本号——`conda install pandas=0.20.3`。配置新工作环境，保持 `python` 版本一致，需要使用命令——`conda create -n workspace python=3.6`，这样就能配置上 `python 3.6` 版本且工作环境名称为 `workspace`。如果需要指定特定的 `package` 和 `python` 一起安装，使用命令：`conda create -n workspace python=3.6 pandas=0.20.3 matplotlib=2.1.0 scipy=0.19.1`

- 激活相关的工作环境名称即可，`source activate workspace`（`Mac` 和 `Linux` 可使用）或者 `activate workspace`（`Windows` 使用）