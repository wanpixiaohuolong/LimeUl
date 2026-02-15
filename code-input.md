# LimeCodeInput 验证码输入框

## 介绍

验证码/密码输入框，支持自定义长度、间距、明文/密文(mask)、提示与错误提示、聚焦光标、下划线模式、禁用系统键盘、指定位置插入符号、最后一位自定义样式等。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-code-input v-model="value" />
<l-code-input v-model="value" :length="6" :mask="false" info="请输入验证码" :error-info="errorInfo" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 密码值 | string | - |
| length | 最大长度 | number | 6 |
| gutter | 格子间距 | string | 20rpx |
| mask | 是否隐藏内容 | boolean | true |
| focused | 是否聚焦（显示光标） | boolean | false |
| line | 是否下划线模式 | boolean | false |
| info / errorInfo | 下方提示/错误提示 | string | - |
| borderColor / width / height / radius | 格子样式 | string | - |
| fontSize / color / bgColor / cursorColor | 文本与光标 | string | - |
| activeBgColor / activeBorderColor | 激活格样式 | string | - |
| disabledKeyboard | 禁用系统键盘 | boolean | false |
| disabledDot | 是否禁止输入 . | boolean | true |
| insertAt | 指定位置插入符号 { index, symbol } | object | - |
| lastElementStyle / lastElementPlaceholder / lastElementPlaceholderStyle | 最后一位样式与占位 | string | - |
| type | input 类型 | string | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | value: string | 值变化时触发 |
| focus | - | 聚焦时触发 |
| finish | value: string | 输入完成时触发 |

## Slots 插槽

| 名称 | 说明 | 参数 |
|------|------|------|
| line | 线条 | { active } |

## 插件标签

- `l-code-input`：组件标签
- `lime-code-input`：演示标签

## 主题定制 CSS 变量

code-input-height、code-input-font-size、code-input-radius、code-input-bg-color、code-input-text-color、code-input-info-color、code-input-error-info-color、code-input-dot-*、code-input-cursor-* 等。
