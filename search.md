# LimeSearch 搜索

## 介绍

搜索框组件，用于输入并提交搜索。支持 v-model、居中、禁用、形状（square/round）、右侧操作按钮与多种事件、插槽自定义。兼容 uniapp/uniappx。

**依赖：** `lime-style`、`lime-shared`、`lime-icon`、`lime-svg`

## 使用

```html
<l-search v-model="value" placeholder="请输入关键字" />
<l-search v-model="value" action="取消" @submit="onSubmit" @action-click="onActionClick" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| value / v-model | 输入值 | string | - |
| action | 右侧操作按钮文字 | string | - |
| center | 内容是否居中 | boolean | false |
| clearable | 是否显示清除控件 | boolean | true |
| disabled / focus | 禁用/聚焦 | boolean | false |
| shape | 形状 square/round | string | - |
| placeholder / placeholderClass / placeholderStyle | 占位符 | string | - |
| leftIcon | 左侧图标 | string | - |
| confirmType | 键盘右下角按钮 | string | search |
| maxlength / maxcharacter | 最大长度 | number | -1/- |
| cursor / cursorSpacing / selectionStart / selectionEnd | 光标与选区 | number | - |
| adjustPosition / alwaysEmbed / confirmHold / holdKeyboard | 键盘与页面行为 | boolean | - |
| type | 拉起键盘类型 | string | - |
| lStyle / padding / radius / height / bgColor | 样式 | string \| object | - |
| fontSize / textColor / iconColor / clearIconColor | 文本与图标 | string | - |
| lContentStyle | 内容节点样式 | string \| object | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| action-click | - | 点击右侧操作按钮 |
| change | value: string | 输入时触发 |
| blur / focus | value: string | 失焦/获焦 |
| clear | - | 点击清除按钮 |
| submit | value: string | 确定搜索时触发 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| left | 自定义左侧内容（搜索框外） |
| action | 自定义右侧内容（搜索框外） |
| left-icon | 自定义左侧图标（框内） |
| right-icon | 自定义右侧图标（框内） |

## 插件标签

- `l-search`：组件标签
- `lime-search`：演示标签

## 主题定制 CSS 变量

--l-search-bg-color、--l-search-text-color、--l-search-height、--l-search-placeholder-color、--l-search-icon-color、--l-search-action-color、--l-search-clear-icon-color、--l-search-square-radius、--l-search-round-radius 等。
