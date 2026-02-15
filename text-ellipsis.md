# LimeTextEllipsis 文本省略

## 介绍

文本省略组件，超出行数省略。支持 rows、content、dots、expandText/collapseText 展开收起、position(start/middle/end)、actionColor、@expand/@collapse、expand/collapse 插槽。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-text-ellipsis content="很长的一段文本..." />
<l-text-ellipsis :rows="2" content="超出两行省略..." />
<l-text-ellipsis content="..." dots="..." />
<l-text-ellipsis :rows="2" expand-text="展开" collapse-text="收起" content="..." />
<l-text-ellipsis :rows="2" position="right" expand-text="展开" collapse-text="收起" />
<l-text-ellipsis action-color="#ff5500" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| rows | 最大行数 | number \| string | 1 |
| content | 文本内容 | string | - |
| dots | 省略符号 | string | … |
| expandText | 展开按钮文字 | string | - |
| collapseText | 收起按钮文字 | string | - |
| position | start/middle/end | string | end |
| actionColor | 展开/收起按钮颜色 | string | - |

## Events 事件

| 名称 | 说明 |
|------|------|
| expand | 展开时 |
| collapse | 收起时 |

## Slots 插槽

default（自定义文本）、expand、collapse。

## 插件标签

- `l-text-ellipsis`：组件标签
- `lime-text-ellipsis`：演示标签

## 主题定制

--l-text-ellipsis-line-height、--l-text-ellipsis-action-color、--l-text-ellipsis-color
