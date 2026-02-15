# LimeCell 单元格

## 介绍

单元格组件，用于列表信息展示与交互。可与 CellGroup 搭配，支持多种布局与样式。

**依赖：** `lime-shared`、`lime-icon`、`lime-style`

## 使用

```html
<l-cell-group>
  <l-cell title="单行标题" note="辅助信息" :arrow="true" />
  <l-cell title="单行标题" :arrow="true" :hover="true" :required="true" />
</l-cell-group>
```

## CellGroup Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| title | 分组标题 | string | - |
| inset | 是否圆角卡片风格 | boolean | false |

## Cell Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| title | 左侧标题 | string | - |
| note | 右侧内容 | string | - |
| description | 标题下方描述 | string | - |
| size | 单元格大小，可选 small | string | - |
| icon | 左侧图标名称 | string | - |
| iconColor / iconSize | 左侧图标颜色/尺寸 | string | - |
| rightIcon / rightIconColor / rightIconSize | 右侧图标 | string | - |
| image | 左侧图片链接 | string | - |
| url | 点击跳转链接 | string | - |
| bordered | 是否显示内边框 | boolean | true |
| required | 是否显示必填星号 | boolean | false |
| arrow | 是否右侧箭头 | boolean | false |
| hover | 是否点击反馈 | boolean | false |
| openType | 跳转类型 | string | navigateTo |
| align | 内容对齐 top/middle/bottom | string | middle |
| imageWidth / imageHeight | 图片宽高 | string | - |
| bgColor | 背景色 | string | - |

## Cell Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| click | event: UniPointerEvent | 点击单元格 |

## Cell Slots 插槽

| 名称 | 说明 |
|------|------|
| title | 自定义左侧标题 |
| note / default | 自定义右侧内容 |
| description | 自定义描述 |
| icon | 自定义左侧图标 |
| rightIcon | 自定义右侧图标 |

## 插件标签

- `l-cell`、`l-cell-group`：组件标签
- `lime-cell`：演示标签

## 主题定制

提供大量 CSS 变量，如 --l-cell-height、--l-cell-bg-color、--l-cell-title-color、--l-cell-group-title-color 等，详见组件文档。
