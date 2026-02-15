# LimeAnchor 滚动锚点

## 介绍

滚动锚点，用于长页导航。两种用法：1）包裹式：l-anchor + l-anchor-section（#header + 默认内容）；2）标记式：l-anchor + l-anchor-mark（uniappx app 不支持，用 anchor-section 代替）。v-model 当前锚点名称，改变时自动滚动到对应锚点。

**依赖：** `lime-shared`

## 使用

```html
<view style="height:300px">
  <l-anchor v-model="activeName" @change="onChange">
    <l-anchor-section name="section1">
      <template #header><text class="section-header">第一部分</text></template>
      <view class="section-content">...</view>
    </l-anchor-section>
    <l-anchor-section name="section2">...</l-anchor-section>
    <l-anchor-section name="section3">...</l-anchor-section>
  </l-anchor>
</view>
<!-- 标记式(uniappx app 不支持) -->
<l-anchor v-model="activeSection" style="height:400px">
  <template v-for="item in sections" :key="item.name">
    <l-anchor-mark :name="item.name" />
    <text>{{ item.title }}</text>
    <view>{{ item.content }}</view>
  </template>
</l-anchor>
```

## l-anchor Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| lClass, lStyle | 类名/样式 | string \| object | - |
| v-model / current | 当前锚点名称 | string | - |
| offset | 顶部偏移(暂不支持) | number | 0 |
| upperThreshold, lowerThreshold | 触顶/触底距离 | number \| string | 50 |

## l-anchor Events

update:current / change(name)、scrolltoupper、scrolltolower、scroll。

## l-anchor Slots

default：多个锚点组件。

## l-anchor-section Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| name | 锚点名称(必填唯一) | string | - |
| lClass, lStyle | 类名/样式 | string \| object | - |

## l-anchor-section Slots

header：锚点头部；default：锚点区域内容。

## l-anchor-mark Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| name | 锚点名称(必填唯一) | string \| number | - |
| lClass, lStyle | 类名/样式 | string \| object | - |

## 插件标签

- `l-anchor`、`l-anchor-section`、`l-anchor-mark`：组件标签
- `lime-anchor`：演示标签

## 主题定制

无单独主题变量
