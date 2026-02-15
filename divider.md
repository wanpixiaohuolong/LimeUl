# LimeDivider 分割线

## 介绍

分割线组件，用于将内容分隔为多个区域。支持水平/垂直、中间插入文本、虚线、自定义颜色。

**依赖：** `lime-style`、`lime-shared`

## 使用

```html
<l-divider />
<l-divider>文本</l-divider>
<l-divider content="文本" align="left" dashed />
<l-divider vertical /> 文本 <l-divider vertical dashed /> 文本
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| dashed | 是否虚线 | boolean | false |
| content | 文本内容 | string | - |
| align | 内容位置 left/right | string | center |
| vertical | 是否垂直分割线 | boolean | false |
| color | 线条颜色 | string | - |
| textColor | 文本颜色 | string | - |

## Events 事件

无

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 自定义文本内容 |

## 插件标签

- `l-divider`：组件标签
- `lime-divider`：演示标签

## 主题定制 CSS 变量

| 变量名 | 默认值 | 描述 |
|--------|--------|------|
| --l-divider-color | $border-color-2 | 分割线颜色 |
| --l-divider-text-color | $text-color-3 | 文本颜色 |
| --l-divider-font-size | 12px | 文本大小 |
| --l-divider-line-height | 20px | 文本行高 |
| --l-divider-line-style | solid | 线条样式 |
| --l-divider-margin | 10px | 外边距 |
