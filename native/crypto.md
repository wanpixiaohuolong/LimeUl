# LimeCrypto 加密

## 介绍

UTS 版 crypto 库：MD5、SHA1/SHA256/SHA512、HMAC-SHA256/SHA1、AES/DES 对称加密、RSA 非对称、编码(UTF8/Hex/Base64)。兼容 uniapp/uniappx。非源码 APP 需自定义基座；iOS/鸿蒙普通授权需源码版。

**依赖：** 付费插件

## 使用

```js
import { useCrypto } from '@/uni_modules/lime-crypto'

const crypto = useCrypto()
crypto.MD5('Hello').toString()
crypto.SHA256('Hello').toString()
crypto.HmacSHA256(message, key).toString()
crypto.AES.encrypt(plaintext, key, { iv, mode: crypto.mode.CBC, padding: crypto.pad.Pkcs7 }).toString()
crypto.AES.decrypt(ciphertext, key, { iv, mode, padding }).toString(crypto.enc.Utf8)
crypto.DES.encrypt(plaintext, key).toString()
crypto.RSA.generateKeyPair(); RSA.setPublicKey(...); RSA.encrypt(...); RSA.setPrivateKey(...); RSA.decrypt(...)
crypto.enc.Base64.stringify(wordArray)
```

## API

useCrypto()。MD5、SHA1、SHA256、SHA512、HmacSHA256、HmacSHA1。AES、DES、RSA。enc(Utf8/Base64/Hex)、mode、pad。

## 插件入口

`lime-crypto`：useCrypto
