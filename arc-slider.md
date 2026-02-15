# LimeArcSlider 环形选择器

## 介绍

环形选择器，用于音量、色相环等场景。支持 v-model 数值、v-model:color 色值、v-model:range 双滑块、色环模式(isHue)。兼容 uniapp/uniappx。**付费组件。**

## 使用

```html
<l-arc-slider v-model="value" />
<l-arc-slider v-model:color="color" :is-hue="true" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model | 当前值 | number | - |
| v-model:color | 当前色值(hex/rgb) | string | - |
| v-model:range | 双滑块值 | number[] | [] |
| size | 尺寸 | number | 300 |
| lineCap | 线段末端样式 | string | round |
| strokeWidth | 活动弧线宽度 | number | 30 |
| strokeColor | 活动弧线颜色 | string | #ffb400 |
| trailWidth / trailColor | 轨道宽与颜色 | number/string | 30/#f5f5f5 |
| dotSize / dotBgColor / dotBorderColor / dotBorderWidth | 滑块样式 | number/string | - |
| max | 最大值(总长) | number | 360 |
| step | 步长 | number | 1 |
| isHue | 是否为色相环 | boolean | false |
| isRange | 是否范围选择(对色环无效) | boolean | false |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | { value, diff } | 分值变化时触发 |

## Slots 插槽

无

## 插件标签

- `l-arc-slider`：组件标签
- `lime-arc-slider`：演示标签
