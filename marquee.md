# LimeMarquee 跑马灯

## 介绍

横向/纵向无缝滚动跑马灯。direction(vertical/horizontal)、speed、delay；为实现无缝滚动，插槽内容数据需两份拼接(如 [...data, ...data])。垂直滚动需设固定高度；水平滚动时子项需设 margin 等间距。uniappx app 需 hb4.53+。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-marquee style="height: 200rpx">
  <view v-for="(item, i) in data" :key="i">...</view>
</l-marquee>
<!-- data 为 [...list, ...list] 两份拼接 -->
<l-marquee direction="horizontal" :speed="520">...</l-marquee>
<l-marquee :speed="100" :delay="2000">...</l-marquee>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| direction | 滚动方向 | string | vertical |
| speed | 滚动速率 | number | 50 |
| delay | 延迟开始(ms) | number | 1000 |

## direction 可选值

vertical（垂直）、horizontal（水平）。

## Slots 插槽

default：跑马灯内容；**数据需两份拼接**以实现无缝滚动。

## 插件标签

- `l-marquee`：组件标签
- `lime-marquee`：演示标签

## 主题定制

无
