# LimeScan 华为扫码

## 介绍

基于华为 ScanKit 的扫码插件，单码模式，支持二维码/条形码多种码制；APP 端可生成二维码。兼容安卓、iOS、鸿蒙、H5。需自定义基座；H5 需 HTTPS；界面为华为默认不可改，不需相册可考虑 lime-scancode。试用后再购买。

**依赖：** 付费插件

## 使用

```js
import { scanCode, createQRCode } from '@/uni_modules/lime-scan'

scanCode({
  success(res) { console.log(res.result, res.scanType) },
  fail(err) {}
})

createQRCode({
  width: 300,
  height: 300,
  content: 'limeui.qcoon.cn',
  success(src) { console.log(src) }
})
```

## API

scanCode(options)：scanType[]、onlyFromCamera、success、fail、complete。返回 result、scanType、charSet、path、rawData。createQRCode(options)：content、width、height、success、fail、complete。

## 插件入口

`lime-scan`：scanCode、createQRCode
