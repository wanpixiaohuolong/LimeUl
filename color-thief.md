# LimeColorThief 图片主色提取

## 介绍

提取图片主色和四边颜色，用于背景融合等。通过 API `getPalette(options)` 调用，仅支持本地图片，网络图需先下载。App 需自定义基座。

**依赖：** 原生能力

## 使用

```js
import { getPalette, type ColorThiefOptions } from '@/uni_modules/lime-color-thief'

getPalette({
  sourceImage: '/static/mv.jpg',
  success(res) {
    console.log('四周颜色【上,右,下,左】', res.edges)
    console.log('主色', res.dominant)
  }
})
```

## API

getPalette(options: ColorThiefOptions)。options 含 sourceImage（本地路径）、success(res) 等。

## 插件标签

非组件，工具 API：`lime-color-thief`。

## 主题定制

无
