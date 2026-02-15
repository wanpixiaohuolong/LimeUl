# LimeKeyboard 虚拟键盘

## 介绍

虚拟键盘组件，支持数字键盘、带右侧栏(custom)、身份证(idcard)、车牌(car)。提供 input/delete/blur/key-up/close 事件、标题、extraKey、beforeClose 异步关闭等。兼容 uniapp/uniappx。

**依赖：** `lime-style`、`lime-shared`、`lime-icon`、`lime-svg`

## 使用

```html
<l-keyboard v-model="value" v-model:visible="visible" @input="onInput" @key-up="onKeyUp" />
<l-keyboard type="custom" v-model:visible="visible" :extraKey="['.']" title="键盘标题" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model | 已输入内容 | string | - |
| v-model:visible | 是否弹出键盘 | boolean | false |
| type | custom/default/car/idcard | string | default |
| safeAreaInsetBottom | 是否适配底部安全区 | boolean | true |
| showDeleteKey | 是否显示删除键 | boolean | true |
| randomKeyOrder | 是否随机按键顺序 | boolean | false |
| extraKey | type=custom 时右侧栏按键，如 ['.'] 或 ['00','.'] | string[] | - |
| closeText / deleteText | 关闭/删除按钮文案 | string | 完成/- |
| maxlength | 最大输入长度 | number | - |
| overlay | 是否显示遮罩 | boolean | false |
| title | 键盘标题 | string | - |
| beforeClose | 关闭前回调，返回 Promise<boolean> | Function | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| delete | - | 点击删除键 |
| input | key: string | 点击按键，回传当前已输入内容 |
| key-up | key: string | 点击按键，回传当前按键字符 |
| close | - | 点击关闭按钮 |
| blur | - | 失焦时 |

## Slots 插槽

无

## 插件标签

- `l-keyboard`：组件标签
- `lime-keyboard`：演示标签

## 主题定制 CSS 变量

--l-keyboard-bg-color、--l-keyboard-color、--l-keyboard-key-bg-color、--l-keyboard-key-height、--l-keyboard-font-size、--l-keyboard-close-bg-color、--l-keyboard-icon-* 等。
