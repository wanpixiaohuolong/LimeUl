# LimePicker 选择器

## 介绍

选择器组件，用于在预设数据中单选。支持单列/多列、级联（l-cascade）、多列联动、v-model、加载与空状态、自定义样式。兼容 uniapp/uniappx。

**依赖：** `lime-style`、`lime-shared`、`lime-loading`

## 使用

```html
<l-picker
  title="标题"
  cancel-btn="取消"
  confirm-btn="确定"
  :columns="columns"
  @confirm="onConfirm"
  @pick="onPick"
  @cancel="onCancel"
/>
<l-picker v-model="values">
  <l-picker-item :options="col1" />
  <l-picker-item :options="col2" />
</l-picker>
```

## Picker Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 当前选中值数组 | string[] \| number[] | - |
| columns | 各列数据，二维数组 | PickerColumn[] | - |
| cancelBtn / confirmBtn | 取消/确认按钮文字 | string | '' |
| cancelStyle / confirmStyle | 按钮样式 | string | - |
| title / titleStyle | 标题 | string | - |
| loading / loadingColor / loadingMaskColor / loadingSize | 加载态 | boolean/string | - |
| itemHeight / itemColor / itemFontSize / itemActiveColor | 项样式 | string | - |
| indicatorStyle | 选中框样式 | string | - |
| maskColors | 遮罩颜色 [start,end] | string[] | - |
| bgColor / groupHeight / radius | 背景与高度 | string | - |

## PickerItem Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| options | 该列选项数组 | PickerColumnItem[] | - |
| value | 当前选中 value | string | - |
| column | 第几列 | number | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| cancel | - | 点击取消 |
| change | value | 选中值变化 |
| confirm | { values, indexs, items } | 点击确认 |
| pick | { values, column, index } | 任意列选中时 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 放置 l-picker-item |
| header / footer | 头部/底部 |
| empty | 无数据时内容 |

## Ref 方法

| 名称 | 返回值 | 说明 |
|------|--------|------|
| confirm | - | 停止滚动并触发 confirm |
| getSelectedOptions | PickerConfirmEvent | 获取当前选中项 |

## 级联 l-cascade

通过 `columns` 的 `children` 实现级联；层级多时建议用 Cascader 组件。

## 插件标签

- `l-picker`、`l-picker-item`、`l-cascade`：组件标签
- `lime-picker`：演示标签

## 主题定制

--l-picker-border-radius、--l-picker-bg-color、--l-picker-toolbar-height、--l-picker-cancel/confirm-color、--l-picker-title-*、--l-picker-group-height、--l-picker-indicator-*、--l-picker-item-*、--l-picker-mask-*、--l-picker-loading-* 等。
