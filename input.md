# LimeInput 输入框

## 介绍

输入框组件，支持多种类型、状态与样式。提供前缀/后缀图标、清除按钮、提示文本、竖向布局、经典边框等。兼容 uniapp/uniappx。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-input v-model="value" placeholder="请输入文字" />
<l-input v-model="value" label="标签" placeholder="请输入" :maxlength="10" tips="最大10字" />
```

## Props 属性（节选）

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| value / modelValue / v-model | 输入值 | string \| number | - |
| label | 左侧文本 | string | - |
| placeholder | 占位符 | string | - |
| type | 类型 text/number/idcard/digit/password 等 | string | - |
| layout | 布局 horizontal/vertical | string | horizontal |
| status | 状态 default/success/warning/error | string | - |
| tips | 下方提示文本 | string | - |
| clearable / clearTrigger | 是否可清空/触发方式 | boolean / string | - |
| disabled / readonly / focus | 禁用/只读/聚焦 | boolean | - |
| align | 文本对齐 left/center/right | string | - |
| prefixIcon / suffixIcon | 前后缀图标（name） | string | - |
| prefixIconColor / suffixIconColor / prefixIconSize / suffixIconSize | 图标样式 | string | - |
| suffix | 后置图标前的内容 | string | - |
| maxlength / maxcharacter | 最大长度 | number | -1/- |
| bordered / classic | 无边框/经典边框 | boolean | - |
| confirmType | 键盘右下角按钮 | string | - |
| cursor / cursorColor / cursorSpacing | 光标相关 | number/string | - |
| lStyle / labelStyle / tipsStyle / inputStyle | 自定义样式 | string \| object | - |
| borderColor / focusedBorderColor | 边框颜色 | string | - |
| clearIconSize | 清除图标大小 | string | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | - | 输入值变化 |
| focus / blur | - | 获焦/失焦 |
| confirm | - | 回车键按下 |
| clear | - | 点击清空 |
| click-icon | - | 点击图标 |
| keyboardheightchange | - | 键盘高度变化 |
| nicknamereview | - | 昵称审核完毕（type=nickname） |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| prefix-icon | 前置图标 |
| label | 标题 |
| suffix | 后置内容 |
| suffix-icon | 后置图标 |
| tips | 提示内容 |

## 插件标签

- `l-input`：组件标签
- `lime-input`：演示标签

## 主题定制

提供 --l-input-padding-*、--l-input-text-color、--l-input-*-tips-color、--l-input-bg-color、--l-input-border-*、--l-input-placeholder-*、--l-input-label-*、--l-input-disabled-*、--l-input-classic-* 等变量。
