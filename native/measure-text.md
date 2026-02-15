# LimeMeasureText 测量文本

## 介绍

测量指定文案在给定字号下的宽高(px)。兼容 web/ios/安卓/鸿蒙 next/微信小程序。需在页面引入后自定义基座。

**依赖：** 付费插件

## 使用

```js
import { measureText } from '@/uni_modules/lime-measure-text'

const [width, height] = measureText('Hello World', 16)
console.log(`宽: ${width}px, 高: ${height}px`)
```

## API

| 方法 | 说明 | 参数 |
|------|------|------|
| measureText | 测量文本尺寸 | (text: string, fontSize: number) => [width, height] |

## 插件入口

`lime-measure-text`：measureText
