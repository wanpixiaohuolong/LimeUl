# LimeLiquid 水波进度球

## 介绍

水波进度球，用于进度、水位、容量百分比展示。v-model:current 为过渡值，支持自定义大小、颜色、外边框(outline)、圆角(radius)、内部背景色(innerColor)。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-liquid v-model:current="current" :percent="target">
  <text>{{ current }}%</text>
</l-liquid>
<l-liquid :percent="60" size="200rpx" />
<l-liquid :percent="70" wave-color="#1989fa" />
<l-liquid :percent="80" outline />
<l-liquid :percent="40" radius="10px" />
<l-liquid :percent="75"><view class="custom">75%</view></l-liquid>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| percent | 进度百分比 | number | 10 |
| size | 尺寸(rpx/px) | string | - |
| outline | 是否显示外边框 | boolean | false |
| radius | 圆角 | string | - |
| waveColor | 波纹颜色 | string | - |
| innerColor | 内部背景色 | string | - |
| duration | 动画时长(ms) | number | 500 |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 进度变化 | percent: number |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 球中间内容 |

## 插件标签

- `l-liquid`：组件标签
- `lime-liquid`：演示标签

## 主题定制

--l-liquid-bg-color、--l-liquid-size、--l-liquid-*-border-radius、--l-liquid-wave-color、--l-liquid-border-*（部分 uniappx app 无效）
