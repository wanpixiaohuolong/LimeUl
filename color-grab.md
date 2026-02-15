# LimeColorGrab 图片取色

## 介绍

基于 canvas 获取图片指定坐标颜色的组件。传入图片地址，点击或滑动取色，通过 change 事件回传颜色值。**付费组件。**

**依赖：** `lime-shared`

## 使用

```html
<l-color-grab src="/static/logo.png" @change="onChange" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| src | 图片地址 | string | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | color: string | 取色时触发 |

## Slots 插槽

无

## 插件标签

- `l-color-grab`：组件标签
- `lime-color-grab`：演示标签

## 主题定制 CSS 变量

--l-color-grab-handle-size、--l-color-grab-handle-border-width、--l-color-grab-handle-border-color
