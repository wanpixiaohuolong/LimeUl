# LimeLayout 布局

## 介绍

通过 `l-row` / `l-col` 划分区块，规范版面布局与信息分布。支持栅格、间距、对齐、宽高比、列顺序等。

**依赖：** `lime-style`、`lime-shared`

## 使用

```html
<l-row>
  <l-col span="8"><text>span: 8</text></l-col>
  <l-col span="8"><text>span: 8</text></l-col>
  <l-col span="8"><text>span: 8</text></l-col>
</l-row>
<l-row gap="20" justify="center" align="center">
  <l-col span="6" offset="2"><text>列</text></l-col>
  <l-col span="auto"><text>自动</text></l-col>
</l-row>
```

## Row Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| gap | 列间距，数字或带单位；数组为 [垂直, 水平] | string \| number \| Array | - |
| justify | 主轴对齐 start/center/end/around/between/evenly | string | start |
| align | 交叉轴对齐 start/center/end/stretch | string | start |
| wrap | 是否换行 | boolean | true |
| lStyle | 自定义容器样式 | string \| Object | - |

## Col Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| span | 列占比 1-24，auto 自动分配，none 按自身尺寸 | number \| string | - |
| offset | 列偏移（基于 24 栅格） | number \| string | 0 |
| order | 排序（数值越大越靠后，uniappx app 无效） | number | 0 |
| aspectRatio | 宽高比 | number | - |
| lStyle | 自定义列样式 | string \| Object | - |

## Events 事件

无

## Slots 插槽

无（子元素直接放在 row/col 内）

## 插件标签

- `l-row` / `l-col`：组件标签（文档中亦写作 l-layout）
- `lime-layout`：演示标签
