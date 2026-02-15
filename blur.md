# LimeBlur 图片高斯模糊

## 介绍

图片高斯模糊处理。两种用法：1）API：gaussianBlur(options)，支持离屏 canvas 或传入 canvasId+component；2）组件：l-blur 配合 src、radius、gaussian。App 需自定义基座。

**依赖：** 见官方文档

## 使用

```js
import { gaussianBlur, type GaussianBlurOptions } from '@/uni_modules/lime-blur'

gaussianBlur({
  src: 'https://...',
  radius: 5,
  success(url) { console.log('处理后', url) }
})
// 非离屏：传 canvasId、component、onSize 等
```

```html
<l-blur :radius="radius" gaussian @success="success" :src="src" />
```

## Props 属性（组件）

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| src | 图片地址 | string | - |
| radius | 模糊半径 | number | 0 |
| gaussian | 是否高斯模糊，false 为堆栈模糊 | boolean | true |

## Events 事件

success(url)、fail(error)。

## GaussianBlurOptions（API）

src、radius、gaussian、canvasId、component、success、fail、onSize(width, height)。

## 插件标签

- `l-blur`：组件标签
- `lime-blur`：演示标签

## 主题定制

无
