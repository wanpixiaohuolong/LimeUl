# LimeRate 评分

## 介绍

评分组件，用于对事物进行评级。支持自定义图标大小、间距、数量、步长、半星、可清空、禁用、自定义选中/未选中图标与颜色。兼容 uniapp/uniappx。**付费组件，需源码运行。**

**依赖：** `lime-shared`、`lime-icon`、`lime-svg`、`lime-style`

## 使用

```html
<l-rate v-model="value" />
<l-rate v-model="value" :count="6" :step="0.5" allow-half clearable />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 当前分值 | number | - |
| count | 图标总数 | number \| string | 5 |
| size | 图标大小(默认 px) | number \| string | 24 |
| gap | 图标间距(默认 px) | number \| string | 4 |
| step | 步长 0-1 | number | 1 |
| color | 选中时颜色 | string | #ffb400 |
| void-color | 未选中时颜色 | string | #c8c9cc |
| icon | 选中时图标名或图片链接 | string | star-filled |
| void-icon | 未选中时图标 | string | - |
| allow-half | 是否允许半选 | boolean | false |
| clearable | 再次点击同值是否清除 | boolean | false |
| disabled / readonly | 禁用/只读 | boolean | false |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | currentValue: number | 分值变化时触发 |

## Slots 插槽

无

## 插件标签

- `l-rate`：组件标签
- `lime-rate`：演示标签

## 主题定制 CSS 变量（uniappx app 无效）

--l-rate-icon-scale、--l-rate-selected-color、--l-rate-unselected-color、--l-rate-disabled-color
