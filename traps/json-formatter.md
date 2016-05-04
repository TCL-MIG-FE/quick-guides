# JSON格式问题

## 问题描述

通过`jQuery`的`$.getJSON`获取`JSON`数据时，成功回掉不执行。换用`$.ajax`方式获取数据，失败回掉执行了，同时提示{% em type="red" %}syntaxError: Unexpected token ' at Object.parse (native) at bI.extend.parseJSON{% endem %}错误


## 原因分析 

后端返回的`JSON`格式不标准，标准的`JSON`格式在描述对象时，必须用双引号扩起来。

```javascript

// bad
var json = "{'name':'larry','age':10}"

// good
var json = '{"name":"larry","age":10}'

```

## 解决方法

修改返回的`JSON`格式，使其标准化。

其实检测一个字符串是否是标准的`JSON`格式很简单，在浏览器里面运行`JSON.parse(str)`即可，如果不报错误，说明`str`是标准的`JSON`字符串。