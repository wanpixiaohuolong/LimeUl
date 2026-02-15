# LimeScrollX 横向滚动

## 介绍

横向滚动容器，底部带滚动指示器。支持 trackWidth/trackHeight/trackColor、barWidth/barColor、indicator 是否显示、@scroll。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-scroll-x>
  <view class="grid">
    <view class="item" v-for="(item, i) in 10" :key="i">...</view>
  </view>
</l-scroll-x>
<l-scroll-x track-width="100px" track-height="6px" track-color="#f5f5f5" bar-width="30px" bar-color="#1989fa" />
<l-scroll-x :indicator="false" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| trackWidth | 轨道宽度 | string | - |
| trackHeight | 轨道高度 | string | - |
| trackColor | 轨道背景色 | string | - |
| barColor | 滑块颜色 | string | - |
| barWidth | 滑块宽度 | string | - |
| indicator | 是否显示指示器 | boolean | true |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| scroll | 滚动时 | event: Event |

## Slots 插槽

default：需横向滚动的内容。

## 插件标签

- `l-scroll-x`：组件标签
- `lime-scroll-x`：演示标签

## 主题定制

--l-scrollx-track-width/height/color、--l-scrollx-bar-color/width
