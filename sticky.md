# LimeSticky 粘性布局

## 介绍

粘性布局组件，实现滚动时吸顶或吸底。在屏幕内正常排列，滚出后固定在顶部或底部。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-sticky>
  <button>基础吸顶</button>
</l-sticky>
<l-sticky :offset-top="40"><button>吸顶距离</button></l-sticky>
<l-sticky :offset-bottom="44"><button>吸底</button></l-sticky>

<l-sticky-box style="height: 300px;">
  <l-sticky><button>容器内吸顶</button></l-sticky>
</l-sticky-box>
```

## Sticky Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| offset-top | 吸顶时与顶部距离，支持 px/rpx | number \| string | 0 |
| offset-bottom | 吸底时与底部距离，支持 px/rpx | number \| string | 0 |
| z-index | 吸顶时的 z-index | number | 99 |
| l-class | 自定义类名 | string | - |
| l-style | 自定义样式 | string \| object | - |
| scrollTop | scroll-view 的滚动位置（仅 uniappx app） | number | - |

## StickyBox Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| l-class | 自定义类名 | string | - |
| l-style | 自定义样式 | string \| object | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | isFixed: boolean | 吸顶/吸底状态改变 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 需要吸顶/吸底的内容 |

## 插件标签

- `l-sticky`、`l-sticky-box`：组件标签
- `lime-sticky`：演示标签

## 主题定制 CSS 变量

| 变量名 | 默认值 | 描述 |
|--------|--------|------|
| --l-sticky-z-index | 99 | 粘性布局层级 |
