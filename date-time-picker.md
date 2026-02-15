# LimeDateTimePicker 时间选择器

## 介绍

时间选择器，用于选择日期、时分等。支持 v-model、start/end 范围、mode 类型组合、format、renderLabel、customFilter。通常与 Popup 搭配使用。

**依赖：** `lime-shared`、`lime-picker`

## 使用

```html
<l-date-time-picker
  v-model="value"
  title="选择日期"
  confirm-btn="确认"
  cancel-btn="取消"
  start="2020-6-30"
  end="2025-6-30"
  @confirm="onConfirm"
  @change="onChange"
/>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 当前选中日期字符串 | string | - |
| start / end | 最小/最大可选时间 | string \| number | 当前±10年 |
| format | confirm 回调的格式化 | string | - |
| mode | 1年 2月 4日 8时 16分 32秒，位组合或中文/英文如"年月日时分" | string \| number | 1\|2\|4 |
| customFilter | 选项过滤函数 (type, columns)=>columns | Function | - |
| renderLabel | 选项格式化 (type, value)=>string | Function | - |
| showUnit | label 后是否显示单位 | boolean | true |
| minHour / maxHour / minMinute / maxMinute | 时分范围 | number | 0/23/0/59 |
| cancelBtn / cancelStyle / confirmBtn / confirmStyle | 按钮 | string | - |
| title / titleStyle | 标题 | string | - |
| itemHeight / itemColor / itemFontSize / itemActiveColor | 项样式 | string | - |
| indicatorStyle / maskColors / bgColor / groupHeight / radius | 样式 | string/string[] | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| cancel | - | 点击取消 |
| change | value: string | 选中变化 |
| confirm | value: string | 点击确认 |
| pick | value: string | 任意列选中 |

## Slots 插槽

无

## 插件标签

- `l-date-time-picker`：组件标签
- `lime-date-time-picker`：演示标签

## 主题定制

与 Picker 共用 --l-picker-* 系列变量，见 Picker 文档。
