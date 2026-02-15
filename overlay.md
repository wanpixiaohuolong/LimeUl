# LimeOverlay 遮罩层

## 介绍

遮罩层组件，用于强调部分内容或配合弹层。支持自定义样式、嵌入内容（默认插槽）、动画时长、关闭时是否销毁。

**依赖：** `lime-style`、`lime-shared`、`lime-transition`

## 使用

```html
<l-overlay :visible="show" @click="show = false" />
<l-overlay :visible="show" @click="show = false">
  <view class="wrapper"><view class="block" /></view>
</l-overlay>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| visible | 是否展示 | boolean | false |
| z-index | 层级 | number | 1000 |
| duration | 动画时长(ms)，0 禁用 | number | 300 |
| lStyle | 自定义样式 | string | - |
| destoryOnClose | 隐藏时是否销毁 | boolean | false |

## Events 事件

| 名称 | 说明 |
|------|------|
| click | 点击遮罩时触发 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 在遮罩上方嵌入内容 |

## 插件标签

- `l-overlay`：组件标签
- `lime-overlay`：演示标签

## 主题定制

--l-overlay-z-index、--l-overlay-bg-color、--l-overlay-blur
