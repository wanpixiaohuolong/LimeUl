# LimeWatermark 水印

## 介绍

水印组件，支持文字(content 单行或数组)、图片(image)、旋转(rotate)、字体样式(font)、间距(gap)、偏移(offset)、全屏(fullScreen)、单块宽高(width/height)、baseSize、fontGap。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-watermark content="LIME UI"><view class="content">页面内容</view></l-watermark>
<l-watermark :content="['LIME UI', '版权所有']">...</l-watermark>
<l-watermark image="https://...">...</l-watermark>
<l-watermark content="LIME UI" :rotate="30" :font="{ color: 'rgba(0,0,0,0.15)', fontSize: 16 }" />
<l-watermark :gap="[60,60]" :offset="[20,20]" />
<l-watermark full-screen />
<l-watermark :width="120" :height="60" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| zIndex | 层级 | number | 9 |
| rotate | 旋转角度 | number | -22 |
| width, height | 单块宽高 | number | - |
| image | 图片地址 | string | - |
| content | 文字，字符串或数组 | string \| string[] | - |
| font | { color, fontSize, fontWeight, fontStyle, fontFamily } | object | - |
| gap | [水平, 垂直] 间距 | number[] | [30,30] |
| offset | [水平, 垂直] 偏移 | number[] | - |
| fullScreen | 全屏水印 | boolean | false |
| baseSize | 图片重复次数 | number | 2 |
| fontGap | 多行文字行间距 | number | 3 |

## Slots 插槽

default：被水印包裹的内容。

## 插件标签

- `l-watermark`：组件标签
- `lime-watermark`：演示标签

## 主题定制

无单独 CSS 变量表（样式通过 props 控制）
