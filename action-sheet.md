# LimeActionSheet 动作面板

## 介绍

动作面板，从底部弹出一组操作选项。支持 list 配置、图标、取消按钮、描述、禁用/着色、宫格型(rowCol)。适用于分享、筛选、操作确认等。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-action-sheet v-model="show" :list="list" @select="onSelect" />
<l-action-sheet v-model="show" :list="list" cancel-text="取消" description="描述信息" @cancel="onCancel" />
<l-action-sheet v-model="show" :row-col="[4, 8]" :list="grid" cancel-text="取消" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / visible | 是否显示 | boolean | false |
| list | 选项列表 ActionSheetItem[] | array | [] |
| title | 顶部标题 | string | - |
| cancel-text | 取消按钮文字 | string | - |
| align | center / left | string | center |
| description | 选项上方描述 | string | - |
| overlay | 是否显示遮罩 | boolean | true |
| safe-area-inset-bottom | 底部安全区 | boolean | true |
| rowCol | 宫格每行列数，如 [4, 8] | number[] | - |
| bordered | 是否显示分割线 | boolean | true |
| closeable | 是否显示关闭图标 | boolean | true |

## list 项 (ActionSheetItem)

| 键名 | 说明 | 类型 |
|------|------|------|
| label | 标题 | string |
| color | 文字颜色 | string |
| icon | 图标名或图片链接 | string |
| iconColor | 图标颜色 | string |
| bgColor | 图标背景色 | string |
| fontSize | 字体大小 | string |
| radius | 图标圆角 | string |
| disabled | 是否禁用 | boolean |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| select | 点击选项 | (index, item) |
| cancel | 点击取消按钮 | - |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 自定义面板内容 |
| description | 自定义描述 |
| title | 自定义标题栏 |

## 插件标签

- `l-action-sheet`：组件标签
- `lime-action-sheet`：演示标签

## 主题定制

--l-action-sheet-item-height、--l-action-sheet-font-size、--l-action-sheet-color、--l-action-sheet-border-radius、--l-action-sheet-* 等，详见官方文档。
