# LimeSlider 滑块

## 介绍

滑块组件，用于在范围内选择数值或区间。支持单滑块、双滑块(range)、垂直、步长、禁用、自定义轨道/滑块样式、反向、禁止双滑块交叉(noCross)、插槽自定义按钮。兼容 uniapp/uniappx。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-slider v-model="value" @change="onChange" />
<l-slider v-model="rangeValue" range noCross />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| modelValue / value / v-model | 当前值，双滑块为数组 | number \| number[] | - |
| min / max | 最小/最大值 | number | 0/100 |
| step | 步长 | number | 1 |
| range | 是否双滑块 | boolean | false |
| disabled / readonly | 禁用/只读 | boolean | false |
| reverse | 是否反向移动 | boolean | false |
| noCross | 双滑块是否禁止交叉 | boolean | false |
| vertical | 是否垂直展示(高度 100% 父元素) | boolean | false |
| thumbSize | 滑块大小 | string | - |
| thumbColor / thumbBorderColor / thumbRadius | 滑块样式 | string | - |
| railColor / railRadius / railSize | 轨道样式 | string | - |
| trackColor | 已选轨道颜色 | string | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | value: number \| number[] | 值变化时触发 |
| dragStart | value | 开始拖动时触发 |
| dragEnd | value | 结束拖动时触发 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| button / startThumb | 自定义滑块按钮 |

## 插件标签

- `l-slider`：组件标签
- `lime-slider`：演示标签

## 主题定制 CSS 变量

--l-slider-rail-size、--l-slider-rail-color、--l-slider-track-color、--l-slider-disabled-color、--l-slider-dot-size、--l-slider-dot-color、--l-slider-dot-radius
