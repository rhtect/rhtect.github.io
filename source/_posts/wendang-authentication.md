---
title: 辅助运输系统身份认证信息
date: 2020-03-03 10:39:01
updated: 2020-03-03 10:39:01
categories: 文档
tags: 辅助运输
password: ruihua123
---

#### 接口身份验证

* APPKEY
> * `用车申请APP` : <font color="red">RUIHUAYCSQ</font>
> * `车载终端APP` : <font color="red">RUIHUACHEZAI</font>

* 用户签名`sign`
> * `userName`
> * `password` 用户密码的SHA1值，<font color="red">用户不存在密码时，默认密码为`#`</font>
> * `UUID` MAC地址去掉冒号，MD5加密
> * `timestamp` 当前时间
> * `appKey`: 应用的APPKEY
```
sign示例：
“张三_7c4a8d09ca3762af61e59520943dc26494f8941b_e10adc3949ba59abbe56e057f20f883e_1571902843_RUIHUAYCSQ”

```

* 接口参数
> * `userName`
> * `appKey`: 应用的APPKEY
> * `timestamp` 当前时间
> * `UUID` MAC地址去掉冒号，MD5加密
> * `APP version`:当前软件的版本号
> * `OS version`：当前操作系统的版本号
> * `Model`：当前手机型号
> * `sign`：用户签名 MD5加密


* 浏览器默认参数
> * `userName` : 用户名
> * `timestamp` : <font color="red">111000</font>
> * `UUID` : <font color="red">000000</font>
> * `APP version` : <font color="red">1.0</font>
> * `OS version` : <font color="red">1.0</font>
> * `Model`: <font color="red">Browser</font>
> * `IP` : <font color="red">127.0.0.1</font>
> * `sign` : `用户签名` MD5加密
