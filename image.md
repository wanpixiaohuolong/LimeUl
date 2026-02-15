# LimeImage 图片加强版

## 介绍

在原生 image 基础上增加加载中/加载失败状态与图片形状（方形、圆角、圆形），支持所有原生 image 属性。

**依赖：** `lime-shared`

## 使用

```html
<l-image mode="widthFix" src="https://example.com/photo.jpg" />
<l-image shape="round" src="..." />
<l-image shape="circle" width="80" height="80" src="..." />
```

## Props 属性

除原生 image 属性外，增强属性如下：

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| src | 图片地址 | string | - |
| mode | 裁剪缩放模式，同原生 | string | - |
| shape | 形状：square/round/circle | string | square |
| width | 图片宽度 | number | - |
| height | 图片高度 | number | - |
| lazy-load | 是否懒加载 | boolean | false |
| fade-show | 是否淡入显示 | boolean | false |
| webp | 是否优先 webp | boolean | false |
| show-menu-by-longpress | 长按显示识别小程序码菜单 | boolean | false |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| load | event.detail: object | 加载成功 |
| error | event.detail: object | 加载失败 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| loading | 自定义加载中内容 |
| error | 自定义加载失败内容 |

## 插件标签

- `l-image`：组件标签
- `lime-image`：演示标签

## 主题定制 CSS 变量

| 变量名 | 默认值 | 描述 |
|--------|--------|------|
| --l-image-color | $text-color-3 | 默认颜色（加载/错误态） |
| --l-image-loading-bg-color | $fill-3 | 加载时背景色 |
| --l-image-loading-color | $text-color-4 | 加载动画颜色 |
| --l-image-round-radius | $border-radius | 圆角半径 |
| --l-image-circle-radius | $border-radius-hg | 圆形半径 |
