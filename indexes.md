# LimeIndexes 索引

## 介绍

索引列表，用于通讯录、城市等快速定位。用法一：l-indexes + l-indexes-section（index + 内容）；用法二：scrollView 局部滚动；用法三：l-indexes-anchor 标记式（APP 可用 sticky-section + list-item）。索引字符从子组件自动收集。支持 sticky、stickyOffset、showTips、color/activeColor/activeBgColor、current、@select/@change。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-indexes :show-tips="true">
  <l-indexes-section index="A">
    <view class="index-item">阿坝 513200</view>
    <view class="index-item">阿拉善 152900</view>
  </l-indexes-section>
  <l-indexes-section index="B">
    <view class="index-item">北京 110000</view>
  </l-indexes-section>
</l-indexes>
<l-indexes scroll-view style="height: 500px">...</l-indexes>
<!-- 标记式 APP 等 -->
<l-indexes :show-tips="true">
  <template v-for="item in list" :key="item.index">
    <l-indexes-anchor :index="item.index" />
    <view v-for="(val, i) in item.children" :key="i">{{ val.name }}</view>
  </template>
</l-indexes>
```

## l-indexes Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| sticky | 索引是否吸顶 | boolean | true |
| stickyOffset | 吸顶距顶部距离 | number | 0 |
| zIndex | 层级 | number | 1 |
| scrollView | 是否使用滚动视图 | boolean | false |
| showTips | 是否显示选中索引提示 | boolean | false |
| color, activeColor, activeBgColor | 索引颜色 | string | - |
| tipsColor, tipsBgColor | 提示颜色/背景 | string | - |
| current | 当前选中索引 | string | - |

## l-indexes Events

| 名称 | 说明 | 回调 |
|------|------|------|
| select | 点击索引 | index: number |
| change | 滚动或索引变化 | name: string |
| update:current | 当前索引更新 | name: string |

## l-indexes-section Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| index | 锚点索引字符 | string | - |
| items | 子项数据 | any[] | - |

## l-indexes-section Slots

default、header、item（{ item, index }）。

## l-indexes-anchor Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| index | 锚点索引字符 | string | - |

## l-indexes-anchor Slots

default。

## l-indexes-view Slots

default（平台适配渲染）。

## 插件标签

- `l-indexes`、`l-indexes-section`、`l-indexes-anchor`、`l-indexes-view`：组件标签

## 主题定制

--l-indexes-sidebar-*、--l-indexes-anchor-*
