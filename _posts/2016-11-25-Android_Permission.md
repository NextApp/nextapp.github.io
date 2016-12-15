---

layout: post
title: 安卓权限整理
tags: [Android,权限]
image: 
   background: triangular.png
---

# Android 权限整理

## 读写权限

* android.permission.WRITE_EXTERNAL_STORAGE 写sd卡的权限 API19开始，APP默认拥有该权限
* android.permission.READ_EXTERNAL_STORAGE 读sd卡的权限 

## 网络权限

* android.permission.INTERNET 访问网络权限 可能会产生GRPS流量
* android.permission.CHANGE_NETWORK_STATE 改变网络状态
* android.permission.CHANGE_WIFI_STATE 开启或者关闭WiFi
* android.permission.ACCESS_NETWORK_STATE 获取网络信息状态，如当前的网络连接是否有效
* android.permission.ACCESS_WIFI_STATE 获取当前WiFi接入的状态以及WLAN热点的信息
* android.permission.CHANGE_WIFI_MULTICAST_STATE 改变WiFi多播状态

## 定位权限

* android.permission.ACCESS_COARSE_LOCATION 允许 API 利用 WiFi 或移动蜂窝数据（或同时利用两者）来确定设备位置。API 返回的位置精确度大约相当于城市街区
* android.permission.ACCESS_FINE_LOCATION 允许 API 利用包括全球定位系统 (GPS) 在内的可用位置提供商以及 WiFi 和移动蜂窝数据尽可能精确地确定位置。

## 联系人权限

* android.permission.READ_CONTACTS 允许应用访问联系人通讯录信息

## 手机电话权限

* android.permission.READ_PHONE_STATE 读取电话状态

## 唤醒手机权限

* android.permission.WAKE_LOCK  允许程序在手机屏幕关闭后后台进程仍然运行
* android.permission.RECEIVE_BOOT_COMPLETED 开机app自动运行
* android.permission.GET_ACCOUNTS 

## 蓝牙权限

* android.permission.BLUETOOTH 允许程序连接配对过的蓝牙设备
* android.permission.BLUETOOTH_ADMIN 允许程序进行发现和配对新的蓝牙设备

## 多媒体权限

* android.permission.FLASHLIGHT 允许访问闪光灯
* android.permission.VIBRATE  允许振动
* android.permission.CAMERA  允许访问摄像头进行拍照

## 系统

* @Deprecated android.permission.GET_TASKS   允许程序获取当前或最近运行的应用
* @Deprecated android.permission.RESTART_PACKAGES   结束任务通过restartPackage(String)方法
* android.permission.SYSTEM_ALERT_WINDOW 显示系统窗口
* @Deprecated android.permission.GET_TASKS 获取当前正在运行的task列表

