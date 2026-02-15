# LimeFab 悬浮按钮

## 介绍

悬浮操作按钮，支持拖拽与磁吸。可通过 v-model:offset 控制位置，axis 控制拖拽方向(x/y/xy/lock)，magnetic 控制磁吸方向(x/y)。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-fab @click="onClick" />
<l-fab axis="xy" magnetic="x" @offset-change="onOffsetChange" />
<l-fab v-model:offset="offset" axis="xy" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model:offset | 位置 [x, y]（Vue2 用 :offset.sync） | number[] | 默认右下角 |
| axis | 拖拽方向：'x' \| 'y' \| 'xy' \| 'lock' | string | y |
| magnetic | 磁吸方向：'x' \| 'y' | string | - |
| gap | 与窗口最小间距(px) | number \| string | 24 |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| custom-click | 点击组件 | UniTouchEvent |
| offset-change | 拖拽导致位置变化 | [x, y] |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 自定义气泡内容 |

## 插件标签

- `l-fab`：组件标签
- `lime-fab`：演示标签

## 主题定制

--l-fab-width、--l-fab-height、--l-fab-initial-gap、--l-fab-icon-size、--l-fab-bg-color、--l-fab-color、--l-fab-z-index、--l-fab-border-radius
