# LimeFloatingPanel 浮动面板

## 介绍

底部浮动面板，可上下拖动浏览内容。支持 anchors 锚点、v-model:height、仅头部可拖(content-draggable)、defaultAnchor、ref.toAnchor(index)。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-floating-panel><view>内容</view></l-floating-panel>
<l-floating-panel v-model:height="height" :anchors="anchors">...</l-floating-panel>
<l-floating-panel :content-draggable="false">...</l-floating-panel>
<l-floating-panel ref="fpRef" /> <button @click="fpRef.toAnchor(1)">跳到1</button>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model:height | 当前显示高度(px)（Vue2 用 :height.sync） | number \| string | 0 |
| anchors | 锚点高度数组(px) | number[] | [100, 0.6*屏高] |
| animation | 是否开启动画 | boolean | true |
| content-draggable | 是否允许拖拽内容区 | boolean | true |
| safe-area-inset-bottom | 底部安全区 | boolean | true |
| defaultAnchor | 默认锚点下标 | number | 0 |
| bgColor | 面板背景色 | string | - |
| barColor | 顶部拖拽条颜色 | string | - |
| duration | 动画时长(ms) | number | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| heightChange | 高度改变且结束拖动 | { height } |
| change | 同上 | { height, index } |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 面板内容 |

## Ref 方法

| 方法 | 参数 | 说明 |
|------|------|------|
| toAnchor | index: number | 跳到指定锚点 |

## 插件标签

- `l-floating-panel`：组件标签
- `lime-floating-panel`：演示标签

## 主题定制

--l-floating-panel-border-radius、--l-floating-panel-header-height、--l-floating-panel-z-index、--l-floating-panel-bg-color、--l-floating-panel-bar-*
