title: Java包装类
author: Jiangxindong
tags:
  - Java
  - 学习笔记
categories:
  - 学习笔记
date: 2020-01-15 16:37:00
---
## 什么是包装类?
我们都对Java中的基本类型很熟悉,基本类型是不具备对象的特性的,比如基本类型不能调用方法,功能很少,为了让基本数据类型也具有对象的特性,java为每个基本类型提供了一个包装类,这样我们就可以像操作对象一样操作基本数据类型
**包装类都在java.lang包内**
**基本类与包装类的对应关系:**

![Not found](/post-img/post-img5.png)

**包装类主要提供了两大类方法:**
1. 将本类型和其他基本类型进行转换的方法
2. 将字符串和本类型及包装类互相转换的方法

## Java中基本类型和包装类之间的转换
基本类型和包装类之间经常需要转换
在JDK1.5引入自动装箱和拆箱的机制后,包装类和基本类型之间的转换就更加轻松便利了
那么什么是装箱和拆箱呢?
**装箱:** 把基本类型转换成包装类,使其具有对象的性质,又可分为手动装箱和自动装箱
```
int i = 0;//定义一个int基本类型值
Integer x = new Integer(i);//手动装箱
Integer y = i;//自动装箱
```
**拆箱:** 和装箱相反,把包装类对象转换成基本类型的值,又可分为手动拆箱和自动拆箱
```
Integer j = new Integer(8);
int m = j.intValue();//手动拆箱为int类型
int n = j;//自动拆箱为int类型
```
## Java中基本类型和字符串之间的转换
在程序开发中,我们经常需要在基本数据类型和字符串之间进行转换
其中,
**基本类型转换成字符串有三种方法:**
1. 使用包装类的toString()方法
2. 使用String类的valueOf()方法
3. 使用一个空字符串加上基本类型,得到的就是基本类型数据对应的字符串

示例:
```
int num = 10;
String str1 = Integer.toString(num);//方法一
String str2 = String.valueOf(c);//方法二
String str3 = c+"";//方法三
```

**将字符串转换成基本类型有两种方法:**
1. 调用包装类的parseXxx静态方法
2. 调用包装类的valueOf()方法转换为基本类型的包装类,会自动拆箱
```
String str = "8";
int num1 = Integer.parseInt(str);//方法一
Integer.valueOf(str);//方法二
```