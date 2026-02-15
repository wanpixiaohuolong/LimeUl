# LimeCheckbox 复选框

## 介绍

复选框组件，支持 v-model、单独使用与组合使用。可选形状（rectangle/circle/line/dot）、自定义颜色与大小、最大可选数、全选/反选。兼容 uniapp/uniappx。

**依赖：** `lime-shared`、`lime-icon`、`lime-style`

## 使用

```html
<l-checkbox v-model="checked">复选框</l-checkbox>
<l-checkbox-group v-model="checkedList" @change="onChange">
  <l-checkbox value="Beijing" label="北京" />
  <l-checkbox value="Shanghai" label="上海" />
</l-checkbox-group>
```

## Checkbox Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| name / value | 标识符与选项值 | string \| number / any | - |
| v-model / checked | 是否选中 | any / boolean | - |
| indeterminate | 是否半选 | boolean | false |
| disabled / readonly | 禁用/只读 | boolean | false |
| checkAll | 标识为「全选」选项 | boolean | false |
| icon | 形状：rectangle/circle/line/dot | string | rectangle |
| label | 主文案 | string | - |
| fontSize / iconSize | 文本与图标大小 | string | - |
| checkedColor / iconBgColor / iconBorderColor | 颜色相关 | string | - |
| iconDisabledColor / iconDisabledBgColor | 禁用态颜色 | string | - |
| labelStyle | label 样式 | string \| object | - |

## CheckboxGroup Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 选中值数组 | string[] \| number[] / any[] | - |
| name | 标识符 | string \| number | - |
| disabled / indeterminate | 禁用/半选 | boolean | false |
| direction | 排列方向 vertical | string | horizontal |
| icon / fontSize / iconSize | 同 Checkbox | string | - |
| checkedColor / iconBgColor 等 | 同 Checkbox | string | - |
| max | 最大可选数 | number | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | currentValue: any | 绑定值变化时触发 |

## Checkbox Slots 插槽

| 名称 | 说明 | 参数 |
|------|------|------|
| default | 自定义文本 | { checked, disabled } |
| icon | 自定义图标 | { checked, disabled } |

## Ref 方法（CheckboxGroup）

| 名称 | 参数 | 返回值 | 说明 |
|------|------|--------|------|
| toggleAll | (checked?: boolean) | - | 全选或反选 |

## 插件标签

- `l-checkbox`、`l-checkbox-group`：组件标签
- `lime-checkbox`：演示标签

## 主题定制

提供 --l-checkbox-icon-size、--l-checkbox-font-size、--l-checkbox-icon-checked-color、--l-checkbox-text-color 等变量，详见组件文档。
