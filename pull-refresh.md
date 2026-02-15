# LimePullRefresh 下拉刷新

## 介绍

下拉刷新组件，可包裹页面或 scroll-view/list-view。v-model 控制是否启用，loading 控制加载状态，达到阈值松手触发 refresh，需在回调里设 loading=false 结束。支持自定义阈值、动画、阻尼、#refresher 插槽。**付费组件。**

**依赖：** `lime-style`、`lime-shared`、`lime-loading`

## 使用

```html
<l-pull-refresh v-model="isEnabled" :loading="loading" @refresh="onRefresh">
  <view class="page">...</view>
</l-pull-refresh>
<l-pull-refresh :loading="loading" @refresh="onRefresh">
  <template #refresher="{ status, progress }">
    <text v-show="status=='pulling'">下拉刷新</text>
    <text v-show="status=='ready'">松手刷新</text>
    <text v-show="status=='loading'">加载中...</text>
    <text v-show="status=='done'">刷新完成</text>
  </template>
  <list-view>...</list-view>
</l-pull-refresh>
```

## 刷新状态

initial、pulling、ready、loading、rebounding、done

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / modelValue | 是否启用 | boolean | true |
| disabled | 禁用（优先于 modelValue） | boolean | false |
| refresherHeight | 提示区域高度 | string \| number | 50 |
| loadingTexts | [下拉中, 可松手, 加载中, 完成] | string[] | 默认文案 |
| maxDrag | 最大下拉高度 | string \| number | 80 |
| loading | 加载状态（需在 refresh 里设为 false） | boolean | false |
| threshold | 触发刷新阈值(px) | number \| string | 50 |
| transitionDuration | 回弹动画(ms) | number | 300 |
| doneDuration | 完成停留(ms) | number | 0 |
| damping | 阻尼 0–1 | number | 0.2 |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| refresh | 达到阈值松手触发 | - |
| update:modelValue | 启用状态变更 | value: boolean |
| update:disabled | 禁用状态变更 | value: boolean |

## Slots 插槽

| 名称 | 说明 | 参数 |
|------|------|------|
| default | 页面/滚动容器 | - |
| refresher | 自定义下拉头部 | { status, progress } |

## 插件标签

- `l-pull-refresh`：组件标签
- `lime-pull-refresh`：演示标签

## 主题定制

--l-pull-refresh-refresher-font-size、--l-pull-refresh-refresher-color、--l-pull-refresh-loading-font-size
