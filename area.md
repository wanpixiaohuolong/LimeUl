# LimeArea 省市区选择

## 介绍

省市区三级联动选择组件，常与弹出层配合。支持本地数据 localData、uniCloud、v-model 绑定地区码、columns-num 控制显示列数（1 省/2 省市/3 省市区）。

**依赖：** `lime-style`、`lime-shared`、`lime-loading`、`lime-picker`

## 使用

```html
<l-area
  v-model="value"
  title="选择地区"
  cancel-btn="取消"
  confirm-btn="确定"
  :local-data="areaList"
  @confirm="onConfirm"
/>
<!-- 使用 uniCloud：<l-area uniCloud /> -->
```

## localData 格式

```js
{
  province_list: { '110000': '北京市', ... },
  city_list:     { '110100': '北京市', ... },
  county_list:   { '110101': '东城区', ... },
}
```

地区码 6 位，前 2 省、中 2 市、后 2 区。可从 `@/uni_modules/lime-shared/areaData` 引入 `areaList`。

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 当前选中地区码数组 | string[] \| number[] | - |
| local-data | 省市区数据对象 | Object | - |
| columns-num | 显示列数 1/2/3 | number | 3 |
| uniCloud | 是否用 uniCloud opendb-city-china | boolean | false |
| cancel-btn / cancel-style / confirm-btn / confirm-style | 按钮 | string | - |
| title / title-style | 标题 | string | - |
| loading / loading-color / loading-mask-color / loading-size | 加载态 | boolean/string | - |
| item-height / item-color / item-font-size / item-active-color | 项样式 | string | - |
| indicator-style / mask-colors / bg-color / group-height / radius | 样式 | string/string[] | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| cancel | - | 点击取消 |
| change | value | 选中变化 |
| confirm | { values, indexs, items } | 点击确认 |

## Ref 方法

| 名称 | 返回值 | 说明 |
|------|--------|------|
| confirm | - | 触发 confirm 事件 |
| getSelectedOptions | PickerConfirmEvent | 获取当前选中项 |

## 插件标签

- `l-area`：组件标签
- `lime-area`：演示标签

## 主题定制

与 Picker 共用 --l-picker-* 变量（uvue app 无效），见 Picker 文档。
