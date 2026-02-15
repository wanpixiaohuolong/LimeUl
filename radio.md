# LimeRadio 单选框

## 介绍

单选框组件，用于一组备选项中单选。支持 v-model、单独/组合使用、形状（circle/line/dot）、自定义颜色与大小、搭配 Cell 使用。Vue2 用 `name` 属性，Vue3 用 `value`。

**依赖：** `lime-style`、`lime-shared`

## 使用

```html
<l-radio allowUncheck>单选框</l-radio>
<l-radio-group v-model="checked" @change="onChange">
  <l-radio value="Beijing" label="北京" />
  <l-radio value="Shanghai" label="上海" />
</l-radio-group>
```

## Radio Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| name / value | 标识符与选项值 | string \| number / any | - |
| allowUncheck | 是否允许取消选中 | boolean | false |
| checked / disabled / readonly | 选中/禁用/只读 | boolean | false |
| icon | 形状：circle/line/dot | string | circle |
| label | 主文案 | string | - |
| fontSize / iconSize | 文本与图标大小 | string | - |
| checkedColor / iconBgColor / iconBorderColor 等 | 颜色相关 | string | - |
| labelStyle | 文本样式 | string \| object | - |

## RadioGroup Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 当前选中值 | string \| number / any | - |
| name | 标识符 | string \| number | - |
| allowUncheck / disabled / readonly | 同 Radio | boolean | - |
| direction | 排列方向 vertical | string | horizontal |
| fontSize / iconSize / checkedColor 等 | 同 Radio | string | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | currentValue: any | 绑定值变化时触发 |

## Radio Slots 插槽

| 名称 | 说明 | 参数 |
|------|------|------|
| default | 自定义文本 | - |
| radio | 整体 | { checked, disabled } |
| icon | 自定义图标 | { checked, disabled } |

## 插件标签

- `l-radio`、`l-radio-group`：组件标签
- `lime-radio`：演示标签

## 主题定制

提供 --l-radio-icon-size、--l-radio-font-size、--l-radio-icon-checked-color、--l-radio-text-color 等变量，详见组件文档。
