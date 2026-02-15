# LimeLoading 加载动画

## 介绍

加载动画组件，支持 circular/spinner 类型，可自定义颜色、大小、文本及垂直排列。适用于各种加载场景。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-loading />
<l-loading type="spinner" color="#1677ff" size="40" />
<l-loading text="加载中..." vertical text-size="16" text-color="#1677ff" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| color | 颜色 | string | '' |
| type | 类型：circular / spinner（nvue 仅 circular） | string | circular |
| size | 图标大小(px)，nvue 仅 string | number \| string | 40rpx |
| text | 加载文本 | string | - |
| textColor | 文本颜色 | string | - |
| textSize | 文本大小(px)，nvue 仅 string | number \| string | - |
| vertical | 是否垂直排列图标与文字 | boolean | false |
| mode | APP 动画模式：animate / raf | string | raf |

## Events 事件

无

## Slots 插槽

无

## 插件标签

- `l-loading`：组件标签
- `lime-loading`：演示标签

## 主题定制

--l-loading-color、--l-loading-size、--l-loading-text-color、--l-loading-text-size。uniappx app 下部分变量无效（基于 canvas）。
