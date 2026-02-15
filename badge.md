# LimeBadge 徽标

## 介绍

徽标/角标，用于数字或红点提示。支持 content、dot 红点、max 超过显示 max+、color、position(top-left/top-right/bottom-left/bottom-right)、offset、独立展示、showZero。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-badge content="5"><view class="box" /></l-badge>
<l-badge dot><view class="box" /></l-badge>
<l-badge content="99" :max="99"><view class="box" /></l-badge>
<l-badge content="5" color="#1989fa" />
<l-badge content="5" position="top-left" />
<l-badge content="5" :offset="[10, 10]" />
<l-badge content="5" />
<l-badge content="0" show-zero />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| content | 徽标内容 | number \| string | - |
| dot | 是否红点 | boolean | false |
| max | 最大值，超出显示 max+ | number | - |
| color | 背景色 | string | - |
| offset | [水平, 垂直] 偏移 | [number \| string, number \| string] | - |
| showZero | content 为 0 是否显示 | boolean | false |
| position | top-left/top-right/bottom-left/bottom-right | string | top-right |

## Slots 插槽

default：被包裹元素；content：自定义徽标内容。

## 插件标签

- `l-badge`：组件标签
- `lime-badge`：演示标签

## 主题定制

--l-badge-size、--l-badge-color、--l-badge-padding、--l-badge-font-*、--l-badge-border-*、--l-badge-bg-color、--l-badge-dot-*
