# LimeTag 标签

## 介绍

标签组件，用于标记与分类。支持 type(primary/success/warning/danger/default)、shape(square/round/mark)、variant(light/outline/light-outline)、icon、size(mini/small/medium/large/extra-large)、closable、maxWidth 省略、color/textColor 自定义、@close。

**依赖：** `lime-shared`、`lime-style`（lime-svg 可选）

## 使用

```html
<l-tag type="primary">品牌色</l-tag>
<l-tag shape="round" type="success">圆角</l-tag>
<l-tag variant="light" type="primary">高亮</l-tag>
<l-tag icon="face-retouching" type="primary">标签</l-tag>
<l-tag size="small" type="primary">小</l-tag>
<l-tag max-width="130px" variant="light">超长省略</l-tag>
<l-tag v-if="show" closable @close="show = false">可关</l-tag>
<l-tag color="#7232dd" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| content | 内容 | string | - |
| type | default/primary/success/warning/danger | string | default |
| shape | square/round/mark | string | square |
| size | mini/small/medium/large/extra-large | string | medium |
| variant | solid/light/outline/light-outline | string | solid |
| closable | 是否可关闭 | boolean | false |
| disabled | 是否禁用 | boolean | false |
| icon | 图标名 | string | - |
| prefix | 前缀 | string | - |
| maxWidth | 最大宽度，超出省略 | string | - |
| color, textColor, fontSize, radius, padding | 自定义样式 | string | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| click | 点击 | event: Event |
| close | 关闭 | event: Event |

## Slots 插槽

default、icon。

## 插件标签

- `l-tag`：组件标签
- `lime-tag`：演示标签

## 主题定制

--l-tag-solid-text-color、--l-tag-*-color、--l-tag-*-padding-*、--l-tag-*-font-size、--l-tag-*-height 等
