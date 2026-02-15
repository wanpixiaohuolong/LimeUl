# LimeTable 表格

## 介绍

表格由 l-table、l-tr、l-td 组成，基于 Flex 布局。支持 bordered、underline、height、borderColor、固定表头(tr fixed)、固定列(td fixed/fixed="right")、列宽 width(等比或带单位)、多级表头(嵌套 l-tr/l-td)、合并行列(嵌套表格实现)。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-table>
  <l-tr style="background:#f5f5f5;">
    <l-td><text class="cell">ID</text></l-td>
    <l-td><text class="cell">姓名</text></l-td>
    <l-td><text class="cell">城市</text></l-td>
  </l-tr>
  <l-tr><l-td>1</l-td><l-td>张三</l-td><l-td>广州</l-td></l-tr>
</l-table>
<l-table bordered /><l-table underline />
<l-table height="400rpx"><l-tr fixed>...</l-tr><l-tr v-for="...">...</l-tr></l-table>
<l-td width="2">等比</l-td><l-td width="100rpx">固定</l-td>
<l-td fixed>左固定</l-td><l-td fixed="right">右固定</l-td>
```

## Table Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| bordered | 显示边框 | boolean | false |
| underline | 行下划线 | boolean | false |
| height | 容器高度 | string | - |
| borderColor | 边框颜色 | string | - |
| lClass, lStyle | 类名/样式 | string \| object | - |

## Tr Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| fixed | 固定表头行 | boolean | false |
| lClass, lStyle | 类名/样式 | string \| object | - |

## Td Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| width | 列宽(等比数字或带单位) | string | - |
| fixed | 列固定 true/'left'/'right' | boolean \| string | false |
| lClass, lStyle | 类名/样式 | string \| object | - |

## Table Events

scrolltoupper、scrolltolower、scroll（同 scroll-view）。

## 插件标签

- `l-table`、`l-tr`、`l-td`：组件标签
- `lime-table`：演示标签

## 主题定制

--l-table-bg-color、--l-table-border-color、--l-table-td-fixed-bg-color、--l-table-fixed-*-shadow、--l-table-tr-fixed-bg-color、--l-table-td-bg-color、--l-table-tr-bg-color
