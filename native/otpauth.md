# LimeOtpauth 多因素认证

## 介绍

TOTP(RFC 6238) 一次性密码，支持 SHA1/SHA256/SHA512、自定义位数与周期、生成 otpauth:// URI。安卓需自定义基座。

**依赖：** 付费插件

## 使用

```js
import { useTOTP, type UseTOTPOptions } from '@/uni_modules/lime-otpauth'

const totp = useTOTP()
totp.generate()

const totp2 = useTOTP({
  secret: 'JBSWY3DPEHPK3PXP',
  algorithm: 'SHA256',
  digits: 8,
  period: 30
})
totp2.generate()
totp2.toString()  // otpauth:// URI，可生成二维码
```

## API

useTOTP(options)。UseTOTPOptions：issuer、label、secret、algorithm、digits、period。实例 generate(options?)、toString()。

## 插件入口

`lime-otpauth`：useTOTP
