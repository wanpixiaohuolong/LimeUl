# LimeOcr 文字识别

## 介绍

多语言 OCR，支持结构化结果(段落/行/元素及位置)。支持本地/临时/缓存路径；网络图需先下载。Web 需安装 tesseract.js。需自定义基座。

**依赖：** 付费插件；Web 需 tesseract.js

## 使用

```js
import { recognizeImage, type OCRRecognizeOptions } from '@/uni_modules/lime-ocr'

recognizeImage({
  url: '/static/ocr/231846.png',
  language: 'zh',  // zh|ja|ko|devanagari，鸿蒙/web 默认中英
  success(res) {
    console.log(res.text)
    res.textBlocks  // 结构化
  },
  fail(err) {}
})
```

## API

recognizeImage(options)。OCRRecognizeOptions：url、language、success、fail。返回 text、textBlocks(段落→lines→elements、bounds)。

## 插件入口

`lime-ocr`：recognizeImage
