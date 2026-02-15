# LimeCall 拨号

## 介绍

参考小程序 makePhoneCall 的 UTS API，用法一致。目前仅 uniappX 安卓，iOS 未测。

**依赖：** 无

## 使用

```js
import { makePhoneCall } from '@/uni_modules/lime-call'

makePhoneCall({ phoneNumber: '10086' })
```

## API

| 方法 | 说明 |
|------|------|
| makePhoneCall(options) | 拨打电话，options.phoneNumber |

## 插件入口

`lime-call`：makePhoneCall
