# LimeScancode 扫码/图片识别

## 介绍

UTS 扫码与图片识别：相机实时扫码、本地图片识别。支持 barCode/qrCode/datamatrix/pdf417。统一 success/fail/complete，可选 rawData。兼容安卓、iOS。非源码需自定义基座；需相机/存储权限。

**依赖：** 无

## 使用

```js
import { scanCode, scanImage } from '@/uni_modules/lime-scancode'

scanCode({
  success(res) { console.log(res.result, res.scanType, res.rawData) },
  fail(err) {},
  complete() {}
})

scanImage({
  path: '/static/qrcode.png',
  success(res) { console.log(res.result) },
  fail(err) {}
})
```

## API

scanCode(options)：onlyFromCamera、success、fail、complete。scanImage(options)：path、success、fail、complete。回调 res：result、scanType、rawData?。

## 插件入口

`lime-scancode`：scanCode、scanImage
