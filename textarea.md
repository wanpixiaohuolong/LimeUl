# LimeTextarea 文本域

## 介绍

多行文本输入组件。支持自动增高、字数统计、标签布局、经典边框等。适用于留言、评论、反馈等场景。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-textarea v-model="value" placeholder="请输入文字" />
<l-textarea v-model="value" label="标签" :maxlength="500" :indicator="true" />
```

## Props 属性（节选）

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 文本值 | string | '' |
| label | 左侧文本 | string | - |
| placeholder | 占位符 | string | - |
| maxlength | 最大字符数，-1 不限制 | number | - |
| indicator | 是否显示字数如 0/140 | boolean | - |
| autosize | 是否自动增高（uniappx 鸿蒙 next 不支持） | boolean | false |
| layout | 布局 vertical/horizontal | string | horizontal |
| disabled / readonly / focus | 禁用/只读/聚焦 | boolean | - |
| bordered | 是否显示外边框 | boolean | true |
| confirmType | 键盘右下角按钮 | string | - |
| adjustPosition / confirmHold / holdKeyboard | 键盘与页面行为 | boolean | - |
| fixed / defaultFixed | 固定定位区域需指定 | boolean | - |
| placeholderStyle | 占位符样式 | string | - |
| lStyle / labelStyle / indicatorStyle / innerStyle | 自定义样式 | string | - |
| classic / borderColor / focusedBorderColor | 经典边框与颜色 | boolean/string | - |
| focused | 是否聚焦态 | boolean | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | value: string | 输入内容变化 |
| focus / blur | event | 获焦/失焦 |
| keyboardheightchange | event | 键盘高度变化 |
| linechange | event | 行高变化 |
| confirm | event | 点击完成 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| label | 自定义标签内容 |

## 插件标签

- `l-textarea`：组件标签
- `lime-textarea`：演示标签

## 主题定制

提供 --l-textarea-padding-*、--l-textarea-text-*、--l-textarea-label-*、--l-textarea-indicator-*、--l-textarea-bg-color、--l-textarea-border-*、--l-textarea-placeholder-*、--l-textarea-disabled-*、--l-textarea-classic-* 等变量。
