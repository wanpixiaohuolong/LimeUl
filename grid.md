# LimeGrid 宫格

## 介绍

宫格布局组件，用于功能入口。支持自定义列数、间距、描述、横向排列、边框、小红点/徽标、卡片风格、页面跳转。

**依赖：** `lime-style`、`lime-shared`

## 使用

```html
<l-grid :column="4">
  <l-grid-item text="标题" image="https://..." />
  <l-grid-item text="标题" icon="star" url="/pages/index/index" />
</l-grid>
<l-grid inset><l-grid-item text="卡片风格" icon="home" /></l-grid>
```

## Grid Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| column | 列数 | number | 4 |
| gutter | 格子间距 | number/string | - |
| inset | 是否圆角卡片风格 | boolean | false |
| align | 内容对齐 left/center | string | center |
| bgColor | 格子背景色 | string | - |
| padding | 格子 padding | string | - |
| hover | 是否点击反馈 | boolean | false |

## GridItem Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| text | 标题 | string | - |
| description | 描述 | string | - |
| icon | 图标名称 | string | - |
| iconColor / prefix / iconSize | 图标相关 | string | - |
| layout | vertical / horizontal | string | vertical |
| image | 图片链接 | string | - |
| url | 跳转链接 | string | - |
| dot | 是否右上角小红点 | boolean | false |
| badge | 右上角徽标内容 | string \| number | - |
| bordered | 是否内边框 | boolean | true |
| disabled | 是否禁用点击反馈 | boolean | false |
| openType | 跳转类型 | string | navigateTo |
| imageWidth / imageHeight | 图片宽高 | string | - |
| bgColor / borderColor / padding | 样式 | string | - |
| lStyle / lImageStyle / lTitleStyle / lDescriptionStyle | 自定义样式 | string \| object | - |
| lClass / lIconClass | 自定义类名 | string | - |

## GridItem Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| click | event: UniPointerEvent | 点击格子 |

## GridItem Slots 插槽

| 名称 | 说明 |
|------|------|
| icon | 自定义图标 |
| title | 自定义标题 |
| description | 自定义描述 |
| extra | 自定义底部额外 |

## 插件标签

- `l-grid`、`l-grid-item`：组件标签
- `lime-grid`：演示标签

## 主题定制

提供 --l-grid-item-padding-top、--l-grid-item-bg-color、--l-grid-item-text-color、--l-grid-item-border-color、--l-grid-inset-* 等变量，详见组件文档。
