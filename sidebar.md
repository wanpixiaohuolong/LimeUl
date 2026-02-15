# LimeSidebar 侧边导航

## 介绍

侧边导航，用于内容区域切换。由 l-sidebar + l-sidebar-item 组成。支持 v-model 当前选中、徽标(dot/badge/badgeProps)、disabled、round/line 样式、@change，可与 l-anchor 配合使用。

**依赖：** `lime-shared`、`lime-style`、`lime-badge`

## 使用

```html
<l-sidebar v-model="active">
  <l-sidebar-item title="标签名称" />
  <l-sidebar-item title="标签名称" />
  <l-sidebar-item title="标签名称" />
</l-sidebar>
<l-sidebar-item title="标签" dot />
<l-sidebar-item title="标签" badge="5" />
<l-sidebar-item title="标签" disabled />
<l-sidebar v-model="active" @change="onChange" />
<l-sidebar round /><l-sidebar line />
```

## Sidebar Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model | 当前选中项索引或 value | number \| string | 0 |
| width | 侧边栏宽度 | string | - |
| fontSize, lineHeight | 字体/行高 | string | - |
| textColor, disabledTextColor | 文本/禁用色 | string | - |
| bgColor | 背景色 | string | - |
| selectedFontWeight, selectedTextColor | 选中样式 | string | - |
| selectedBorderWidth, selectedBorderHeight, selectedBorderColor | 选中左侧边框 | string | - |
| selectedBgColor | 选中背景 | string | - |
| round | 圆角样式 | boolean | false |
| line | 线条样式 | boolean | false |

## Sidebar Events

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 切换时 | value: string \| number |

## SidebarItem Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| title | 标题 | string | - |
| value | 唯一标识，空则用下标 | string \| number | - |
| dot | 右上角红点 | boolean | false |
| badge | 徽标内容 | number \| string | - |
| disabled | 禁用 | boolean | false |
| badgeProps | 徽标属性(透传 Badge) | object | - |

## SidebarItem Events

| 名称 | 说明 | 回调 |
|------|------|------|
| click | 点击 | value: string \| number |

## SidebarItem Slots

title、default。

## 插件标签

- `l-sidebar`、`l-sidebar-item`：组件标签
- `lime-sidebar`：演示标签

## 主题定制

--l-sidebar-width、--l-sidebar-height、--l-sidebar-bg-color、--l-sidebar-selected-*、--l-sidebar-font-size、--l-sidebar-text-color、--l-sidebar-padding-*
