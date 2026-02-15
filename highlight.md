# LimeHighlight 文本高亮

## 介绍

文本高亮组件，用于在 text 中高亮 keywords。支持多关键词数组、autoEscape、caseSensitive、highlightStyle/unhighlightStyle、highlightClass/unhighlightClass、default 插槽自定义每段渲染(item.text, item.highlight)。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-highlight text="这是一段包含关键词的文本" keywords="关键词" />
<l-highlight text="..." :keywords="['关键词','示例']" />
<l-highlight keywords="关键词" highlight-style="color:#ff5500; font-weight:bold;" />
<l-highlight highlight-class="custom-highlight" unhighlight-class="custom-text" />
<l-highlight keywords="生活" text="...">
  <template #default="{ item }"><text :style="{ color: item.highlight ? '#07c160' : '#8e69d3' }">{{ item.text }}</text></template>
</l-highlight>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| text | 原始文本 | string | "" |
| keywords | 高亮词，字符串或数组 | string \| string[] | [] |
| autoEscape | 自动转义正则特殊字符 | boolean | true |
| caseSensitive | 区分大小写 | boolean | false |
| highlightStyle | 高亮样式 | string \| object | - |
| unhighlightStyle | 普通文本样式 | string \| object | - |
| highlightClass | 高亮类名 | string | '' |
| unhighlightClass | 普通类名 | string | '' |

## Slots 插槽

| 名称 | 说明 | 参数 |
|------|------|------|
| default | 自定义每段 | { item: { text, highlight, start, end } } |

## 插件标签

- `l-highlight`：组件标签
- `lime-highlight`：演示标签

## 主题定制

--l-highlight-text-color、--l-highlight-normal-color
