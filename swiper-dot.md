# LimeSwiperDot 轮播图指示点

## 介绍

轮播指示器，需配合 swiper 的 current 与 @change 使用。支持 type(dot/dot-bar/index/title/fraction)、total、current、list+field(title 类型)、color/activeColor/inactiveColor、fontSize。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<view style="position:relative">
  <swiper :current="current" @change="onChange" :autoplay="true">
    <swiper-item>1</swiper-item><swiper-item>2</swiper-item><swiper-item>3</swiper-item>
  </swiper>
  <l-swiper-dot :current="current" type="dot" :total="3" />
</view>
<l-swiper-dot :current="current" type="dot-bar" :total="3" />
<l-swiper-dot :current="current" type="index" :total="3" />
<l-swiper-dot :current="current" type="fraction" :total="3" />
<l-swiper-dot :current="current" type="title" :list="list" field="title" />
<l-swiper-dot active-color="#ff6b6b" inactive-color="#ffe66d" color="#2d3436" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| type | dot/dot-bar/index/title/fraction | string | - |
| total | 轮播项总数(非 title) | number | 0 |
| current | 当前激活索引 | number | 0 |
| field | title 类型时的字段名 | string | - |
| list | 数据源(title 类型) | Array | [] |
| color | 全局文本颜色 | string | - |
| activeColor | 激活指示点颜色 | string | - |
| inactiveColor | 未激活颜色 | string | - |
| fontSize | 文字大小 | string | - |

## 插件标签

- `l-swiper-dot`：组件标签
- `lime-swiper-dot`：演示标签

## 主题定制

--l-swiper-dot-fraction-*、--l-swiper-dot-title-*、--l-swiper-dot-radius、--l-swiper-dot-text-color、--l-swiper-dot-bg-color、--l-swiper-dot-*-size、--l-swiper-dot-gap
