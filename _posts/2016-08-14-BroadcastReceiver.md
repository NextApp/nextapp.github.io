---

layout: post
title: BroadcastReceiver解析
tags: [Android]

image: 
   background: triangular.png
---
# BroadcastReceiver解析

## 类说明
如果不是进程间通信，最好使用LocalBroadcastManager这个类去发广播。LocalBroadcastManager在进程内通信
更有效，而且可以避免出现安全性问题。

### 注册
注册方式有两种：

* 动态注册： Context.registerReceiver()

* 静态注册： 在AndroidManifestReceiver直接声明注册。
【注意】如果在activity的onResume()里注册，那么你应该在onPause()里注销。



### 发送方式
* sendBroadcast(Intent) 完全无序异步，大部分情况下所有的接收者同时收到，这样很高效。
