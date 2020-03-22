# R-A-M-D-D3-S-M-H
Python3实现RSA-AES-MD5-DES-DES3-MD5-SHA-HMAC已验证，附带说明

始于前端js对密码加密实现的需要，目前使用最多是AES、RSA、MD5，当然这三个的嵌套和混合使用情况也比较多。

这应该是Python3目前最全的整理，所有案列都亲自测试可行，并标注了使用的一些注意事项和说明。

目前总结有下面几点：

对称加密（加密解密密钥相同）：DES、DES3、AES

非对称加密（分公钥私钥）：RSA

信息摘要算法/签名算法：MD5、HMAC、SHA

前端实际使用中MD5、AES、RSA使用频率是最高的

几种加密方式配合次序：采用非对称加密算法管理对称算法的密钥，然后用对称加密算法加密数据，用签名算法生成非对称加密的摘要

DES、DES3、AES、RSA、MD5、SHA、HMAC传入的消息或者密钥都是bytes数据类型，不是bytes数据类型的需要先转换；密钥一般是8的倍数

Python实现RSA中，在rsa库中带有生成签名和校对签名的方法

安全性：DES<DES3=AES<RSA,至于MD5、SHA、HMAC不好说了
