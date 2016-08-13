---
layout: post
title: 常用工具命令笔记
tags: [Command]

image:
  background: triangular.png
---


# 常用工具命令笔记


## MVN
* 提交文件到远程仓库

	命令：mvn deploy:deploy-file -Dfile=AMap_2DMap_V2.9.0_20160525.jar -DgroupId=com.amap.api -DartifactId=amap_2dmap -Dversion=2.9.0 -Dpackaging=jar -Durl=http://ipAddress/nexus/content/repositories/releases/ -DrepositoryId=Releases

---

## Git

* git reflog : 显示本地分支提交历史
* git branch -D develop : 删除develop分支
* git reset 612d24 : 还原到612d24提交状态
* git branch : 显示所有本地分支
* git branch test : 创建test分支
* git checkout test : 切换到test分支上
* git pull : 拉取远程分支的代码更新到本地
* git pull origin test : 拉取远程test分支的代码更新到本地
* git add . :把当前目录下的文件添加到git仓库中
* git commit -m "nothing" :提交本次修改的内容

---

## Git Flow
* git flow init # 默认各选项,其他TAG > tuyasmart_
* git flow feature start xxxxxxx
* git flow feature finish xxxxxx
* git flow release start v2.5.0r34 # v 版本号, r 内部版本号
* git flow release finish v2.5.0r34
* git flow hotfix start v2.5.1r35 # v 版本号, r 内部版本号
* git flow hotfix finish v2.5.1r35
* git push origin :xxxxx   删除远程库
* git tag -a v2.5.1r35 -m "v2.5.1r35"
* git tag <tag name> <tag name> -f -m "<new message>"
* git push --tags 提交tag"

---

## Vim

### ex命令
* :w 保存
* :q 退出
* :q! 不保存退出
* :h vim帮助
* ZZ 保存退出
* ZQ 不保存退出

### 操作
* d 删除单个字母
* D 删除至行尾
* d2d 删除2行
* A 在行尾附加
* a 在当前光标后附加
* y 拷贝
* Y 拷贝整行
* P 粘贴前
* p 粘贴后
* I 到行首插入
* i 插入模式
* O 分段前
* o 分段后
* u 撤销命令
* CTRL+r 反撤销命令
* J 合并两行
* : ex命令
* X 退格
* x 删除字符
* R 替换模式
* r 替换字符
* shift + -> 删除当前行

### 动作
* W 下一个单词
* w 下一个单词
* E 词尾
* e 词尾
* h 向左移动光标
* j 向下移动光标
* k 向上移动光标
* l 向右移动光标
* B 前一个单词
* b 前一个单词
* L 移动光标到屏幕最后一行
* ( 句首
* ) 句尾
* { 段首
* } 段尾
* \| 行首
* M 屏幕中间 
* gg 文首
* H 屏幕顶行
* G 文尾
* G20G 到第20行

### NERD
* :help NERD_tree.txt 查看NERD 目录插件的帮助
* :NERDTree[<start-directory>\|<bookmark>] 开启目录树
* :NERDTreeClose 关闭目录树

---

## ADB
* adb install 安装软件
* adb install -r 强制安装软件
* adb help 帮助
* adb shell 手机shell模式
* adb uninstall <软件包名> 卸载软件
* adb uninstall -k <软件报名> 卸载软件，但保留配置和缓存文件
* adb devices 查看设备
* adb push <本地路径> <远程路径> 发送文件到设备
* adb pull <远程路径> <本地路径> 从设备上下载文件

---

## 常用Linux命令

* ifconfig 查看ip地址
* pwd 显示目录路径
* ls 显示当前目录下的所有文件
* cd 到某个目录下
* rm 删除文件
* mkdir 创建目录
* mv <文件原始路径> <目标路径> 移动文件
* cp <文件原始路径> <目标路径> 复制文件
* lsof -wni tcp:4000 显示当前正在使用4000端口的进程信息
* kill -9 PID： 杀死当前PID的进程

## Jekyll
* bundle exec jekyll serve 启动jekyll服务