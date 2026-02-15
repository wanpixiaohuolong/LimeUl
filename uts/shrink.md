# LimeShrink 图片压缩

## 介绍

多端图片压缩，非 web 用 uni.compressImage，web 对齐其 API。支持单张/批量、质量、压缩宽高。Web 建议传 File 或带后缀路径以区分 jpg/png 算法。

**依赖：** 无

## 使用

```js
import { compressImage } from '@/uni_modules/lime-shrink'

compressImage({
  src: res.tempFilePaths[0],  // 或 res.tempFiles[0]（Web）
  quality: 75,
  compressedWidth: 500,
  compressedHeight: 300,
  algorithm: 'jpeg',
  success(res) { console.log(res.tempFilePath) },
  fail(err) {},
  complete() {}
})
```

## API

compressImage(options)。LimeShrinkImageOptions：src(string|File)、quality(0-100，默认 80)、compressedWidth、compressedHeight、algorithm('jpeg'|'png')、success、fail、complete。success 回调：tempFilePath、errMsg。

## 插件入口

`lime-shrink`：compressImage；组件 l-shrink（旧版不推荐）
