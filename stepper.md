# LimeStepper 步进器

## 介绍

步进器组件，通过加减按钮或输入框调整数值。支持步长、整数/小数、禁用、禁用输入、多尺寸、多主题、长按连续加减。兼容 uniapp/uniappx。

**依赖：** `lime-style`、`lime-icon`、`lime-shared`

## 使用

```html
<l-stepper v-model="value" />
<l-stepper v-model="value" :step="2" :min="0" :max="100" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| value / v-model / defaultValue | 当前值/默认值 | number | - |
| longPress | 是否开启长按连续加减 | boolean | true |
| disableInput | 禁用输入框 | boolean | false |
| disabled / readonly | 禁用/只读 | boolean | false |
| inputWidth | 输入框宽度 | string | - |
| integer | 是否仅允许整数 | boolean | true |
| max / min | 最大/最小值 | number | 100/0 |
| size | 尺寸 small/medium/large 或具体数值 | string | medium |
| step | 步长 | number | 1 |
| theme | 风格 normal/filled/outline/solid | string | filled |
| iconRadius | 按钮圆角 | string | - |
| minusStyle / plusStyle / inputStyle | 按钮与输入框样式 | object | - |
| cursorColor | 光标颜色 | string | rgba(0,0,0,0.88) |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | value: number | 当前值变化时触发 |
| focus / blur | event: Event | 输入框聚焦/失焦 |
| overlimit | - | 点击加减达上限/下限时触发 |

## Slots 插槽

无

## 插件标签

- `l-stepper`：组件标签
- `lime-stepper`：演示标签

## 主题定制

提供 --l-stepper-*-height、--l-stepper-*-font-size、--l-stepper-*-icon-size、--l-stepper-*-input-width、--l-stepper-border-*、--l-stepper-input-color、--l-stepper-solid-bg-color、--l-stepper-button-bg-color 等变量。
