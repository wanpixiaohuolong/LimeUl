# LimeSwipeCell 滑动单元格

## 介绍

左右滑动展示操作区的单元格组件。支持 left/right 插槽、默认打开状态(opened)、异步关闭(before-close)、禁用、点击外部关闭(closeOnClickOutside)。适用于列表项编辑、删除、收藏等。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-swipe-cell>
  <l-cell title="左滑单操作" :bordered="false" />
  <template #left><view class="btn select-btn">选择</view></template>
  <template #right><view class="btn delete-btn">删除</view></template>
</l-swipe-cell>
<l-swipe-cell :opened="true">...</l-swipe-cell>
<l-swipe-cell :before-close="beforeClose">...</l-swipe-cell>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| name | 标识符 | string | - |
| disabled | 是否禁用滑动 | boolean | false |
| closeOnClickOutside | 点击外部是否关闭（APP/WEB 有效） | boolean | false |
| left | 左侧操作项配置 SwipeActionItem[] | array | - |
| right | 右侧操作项配置 | array | - |
| opened | 是否默认打开，可 [left, right] 分别控制 | boolean \| boolean[] | false |
| before-close | 关闭前回调，返回 Promise\<boolean\> | (direction) => Promise\<boolean\> | - |
| l-style | 自定义样式 | string \| object | - |

## SwipeActionItem

text、icon、className、style、onClick

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| open | 打开时 | direction: 'left' \| 'right' |
| close | 关闭时 | - |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 主内容 |
| left | 左侧滑动区 |
| right | 右侧滑动区 |

## Ref 方法

| 方法 | 说明 |
|------|------|
| close | 关闭滑动单元格 |

非 APP/WEB 可通过 `closeOutside()` 关闭所有已打开的滑动单元格。

## 插件标签

- `l-swipe-cell`：组件标签
- `lime-swipe-cell`：演示标签
