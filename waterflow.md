# LimeWaterflow 瀑布流

## 介绍

瀑布流布局组件，支持虚拟滚动、下拉刷新、自动布局、加载更多。兼容 uniapp/uniappx。**付费组件。**

**依赖：** `lime-style`、`lime-shared`

## 使用

```html
<l-waterflow
  :crossAxisCount="2"
  :mainAxisGap="10"
  :crossAxisGap="10"
  :padding="[10,10,10,10]"
  @scrolltolower="onLoadMore"
  refresherEnabled
  @refresherrefresh="onRefresh"
>
  <l-flow-item v-for="(item, i) in list" :key="i">
    <view class="item">{{ item.title }}</view>
  </l-flow-item>
</l-waterflow>
```

**动态高度内容：** 使用 `content` 插槽，在图片等加载完成后调用 `measure` 以正确计算布局。

## Waterflow Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| crossAxisCount | 列数 | number | - |
| mainAxisGap | 行间距 | number | - |
| crossAxisGap | 列间距 | number | - |
| padding | 内边距 [top,right,bottom,left] | number[] | - |
| bounces | 是否回弹 | boolean | - |
| upperThreshold | 距顶触发 scrolltoupper(px) | number | - |
| lowerThreshold | 距底触发 scrolltolower(px) | number | - |
| scrollTop | 竖向滚动位置 | number | - |
| showScrollbar | 是否显示滚动条 | boolean | - |
| refresherEnabled | 是否下拉刷新 | boolean | false |
| refresherThreshold / refresherMaxDragDistance | 下拉刷新相关 | number | - |
| refresherDefaultStyle | black/white/none | string | - |
| refresherTriggered | 当前下拉刷新状态 | boolean | false |
| virtualScroll | 是否虚拟滚动 | boolean | - |
| preloadScreens | 预加载屏幕数 | number | - |

## FlowItem Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| type | 项目类型 | number | - |
| index | 项目索引 | number | - |

## Waterflow Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| scrolltoupper | event: UniScrollToUpperEvent | 滚动到顶部 |
| scrolltolower | event: UniScrollToLowerEvent | 滚动到底部 |
| refresherrefresh | event: UniRefresherEvent | 下拉刷新 |
| refresherrestore | event: UniRefresherEvent | 下拉刷新复位 |
| refresherpulling | event: UniRefresherEvent | 下拉中 |

## Slots 插槽

**Waterflow：** default（内容项）、refresher（自定义下拉刷新）、load-more（自定义加载更多）  
**FlowItem：** default（项目内容）、content（内容插槽，参数 `{ measure }`，用于动态高度时在加载完成后调用 measure）

## 插件标签

- `l-waterflow`、`l-flow-item`：组件标签
- `lime-waterflow`：演示标签

## 主题定制 CSS 变量

--l-waterflow-height、--l-waterflow-width、--l-waterflow-gap、--l-waterflow-columns、--l-waterflow-bg-color、--l-flow-item-width、--l-flow-item-top/left、--l-flow-item-anim-duration 等。
