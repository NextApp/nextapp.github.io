---
layout: post
title: LocalBroadcastManager解析
tags: [Android]
image: 
   background: triangular.png
---
# LocalBroadcastManager解析

## 类说明
 该类主要用于进程内注册和通过intent发送广播,相对于发送全局广播，LocalBroadcastManager有以下优点：
 
 * 因为数据是私有，所以不会泄露数据
 * 因为不会被其他应用使用，所以不会有安全漏洞而被黑客利用
 * 效率更高

i## 初始化
 LocalBroadcastManager 是一个单例,从代码中可以看出LocalBroadcastManager一旦被使用，其生命周期遍
 和application 保持一致。

```
public static LocalBroadcastManager getInstance(Context context) {
	  synchronized (mLock) {
		 if (mInstance == null) {
			 mInstance = new LocalBroadcastManager(context.getApplicationContext());
		 }
		 return mInstance;
	}
}

```

## 方法分析

```
	//注册本地广播 intentFilter用于事件过滤
	registerReceiver(BroadcastReceiver receiver, IntentFilter filter);
	//发送广播 使用Handler 在主线程内执行相应的recevier。
	sendBroadcast(Intent intent);
	//发送广播 同步处理
	sendBroadcastSync(intent);
	//注销广播 之前所有该广播注册的filters都会被移除
	unregisterReceiver(BroadcastReceiver receiver);

```

## 总结
LocalBroadcastManager类似于EventBus，都是基于观察者模式，用于进程内通信。与EventBus相比，虽然效率略高效，但功能单一，没有异步、后台线程、主线程、调用线程的随意切换。相比之下，EventBus更好。
