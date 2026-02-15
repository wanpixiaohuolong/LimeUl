# LimeFitSwiper 自适应高度轮播

## 介绍

仿金刚区根据内容自适应高度的轮播。由 l-fit-swiper + l-fit-swiper-item 或 data + group 插槽使用。支持 data 数据源、current、indicatorDots、indicatorWidth/Height/Color/ActiveColor、@change。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-fit-swiper :data="list">
  <template #group="{ group }">
    <view class="grid">
      <view class="item" v-for="item in group" :key="item.name">
        <image :src="item.icon" mode="widthFix" /><text>{{ item.name }}</text>
      </view>
    </view>
  </template>
</l-fit-swiper>
<l-fit-swiper indicator-color="#ccc" indicator-active-color="#f00" :data="indicatorList" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| data | 轮播数据(二维数组) | Array | [] |
| current | 当前滑块索引 | number | 0 |
| indicatorDots | 是否显示指示器 | boolean | true |
| indicatorWidth | 指示器项宽度 | string | - |
| indicatorHeight | 指示器高度 | string | - |
| indicatorColor | 指示器颜色 | string | - |
| indicatorActiveColor | 激活颜色 | string | - |
| lClass | 自定义类名 | string | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 轮播切换 | index: number |

## Slots 插槽

default：直接放 l-fit-swiper-item(仅 WEB/APP)；group：按 data 分组渲染，参数 { group }。

## 插件标签

- `l-fit-swiper`、`l-fit-swiper-item`：组件标签
- `lime-fit-swiper`：演示标签

## 主题定制

--l-fit-swiper-indicator-*、--l-fit-swiper-padding-bottom
