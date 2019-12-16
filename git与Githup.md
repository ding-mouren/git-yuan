### git与Githup

#### git

##### git介绍

Git:版本控制器

优点：

- 开源的分布式的版本控制系统，用于敏捷高效地处理任何或小或大的项目。

git命令与Linux兼容

###### 工作流程图

![git工作流程图](C:\Users\丁会想\Desktop\笔记md\图片\git工作流程图.png)

##### 使用版本控制器的原因

##### 本地库与远程库

- 团队内使用：

![git本地库与远程库关系](C:\Users\丁会想\Desktop\笔记md\图片\git本地库与远程库关系.png)

##### git命令行操作

###### 本地库操作

- 初始化：

> git init

**注意：** .git 目录中存放的是本地库相关的子目录与文件，不要删除，也不要胡乱修改

- 设置签名：

> 形式：用户名：ding-mouren
>
> E-mail地址：18856726792@163.com
>
> 命令：
>
> - 项目级别：仅在本地库范围内有效
>   - git config user.name ding-mouren
>   - git config user.email 18856726792@163.com
>   - 信息保存位置：**cat ./.git/config**
> - 系统用户级别：登录当前操作系统的用户范围
>   - git config --global user.name ding-mouren
>   - git config --global user.email 18856726792@163.com
>   - 信息保存位置：**cat  ~/.gitconfig**
> - 级别优先级：
>   - 就近原则：项目优先于系统用户级别
>   - 二者都没不允许

作用：区分不同开发人员的身份

- 状态查看：git status

  - 查看工作区、暂存区状态

- 添加操作：git add 【file name】

  - 将工作区的“新建或修改”添加到暂存区

- 提交操作：git commit -m "commit message" 【file name】（git commit 【file name】：会进入vim模式填写commit message）

  - 将暂存区的内容添加到本地库

- 查看历史

  - git log
  - git reflog
  - git log --pretty=oneline
  - git log --oneline

- 前进后退历史版本

  - 基于索引值：git reset --hard 【局部索引值】（可以前进也可以后退）

  ![搜狗截图20191214174109](C:\Users\丁会想\Desktop\学习产生的废图片\搜狗截图20191214174109.png)

  - 其他方式：

    - 使用^符号：只能后退  **注意：** 一个符号表示后退一步

      > git reset --hard HEAD^^^(后退三步)

    - 使用~符号：只能后退

    > git reset --hard HEAD~3(后退三步)

  - reset三个参数对比：

    - --soft参数：仅仅在本地库移动HEAD指针

    - --mixed参数：在本地库移动HEAD指针

      ​			重置暂存区

    - --hard：在本地库移动HEAD指针

      ​	      重置暂存区

      ​	      重置工作区

- ​

###### 远程库操作



#### GitHub

代码托管中心：GitHub与码云

- 目的：借助GitHub托管项目代码

##### 基本概念

- 仓库（repository）：同来存放项目代码，
- 收藏（star）：
- 复制克隆项目（fork）：

