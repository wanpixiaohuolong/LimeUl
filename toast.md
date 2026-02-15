# LimeToast 轻提示

## 介绍

轻量级 Toast，不打断操作。需在页面放置 `l-toast-agent`，通过 API 调用：toast()、success()、warning()、error()、loading()、hide()、hideAll()。**付费组件。**

**依赖：** `lime-style`、`lime-shared`、`lime-overlay`、`lime-icon`

## 使用

```html
<template>
  <l-toast-agent />
</template>
```

```ts
import { toast, success, warning, error, loading, hide, hideAll } from '@/uni_modules/lime-toast'

toast('提示信息')
toast({ message: '提示', duration: 2000, position: 'middle' })
success('操作成功')
warning('警告')
error('操作失败')
loading('加载中...')  // 默认不自动关闭，需 hide()
setTimeout(() => hide(), 3000)
hideAll()
```

## 函数 API

| 函数 | 说明 |
|------|------|
| toast | options \| message，显示普通提示 |
| success / warning / error | (message, options?) 预设类型 |
| loading | (message, options?) 加载提示，默认 duration=0 |
| hide | (selector?) 关闭当前 |
| hideAll | (selector?) 关闭全部 |

## ToastOptions 配置项

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| message | 提示内容 | string | '' |
| type | success / warning / error / loading | string | - |
| duration | 时长(ms)，0 不自动关闭 | number | 2000 |
| position | top / middle / bottom | string | middle |
| direction | row / column（图标与文字） | string | column |
| overlay | 是否遮罩 | boolean | false |
| overlayStyle | 遮罩样式 | string \| object | - |
| preventScrollThrough | 防止触摸穿透 | boolean | - |
| zIndex | 层级 | number | - |
| icon / iconColor / iconSize / iconPrefix | 自定义图标 | string | - |
| selector | 选择器 | string | - |

## 组件说明

| 组件 | 说明 |
|------|------|
| l-toast | 单条 Toast 内容 |
| l-toast-agent | 页面内放置一个，管理实例显示/隐藏 |
| lime-toast | 演示组件 |

## 注意

每页仅放一个 l-toast-agent；loading 需手动 hide()；支持多实例依次排列。

## 主题定制

--l-toast-color、--l-toast-z-index、--l-toast-bg-color、--l-toast-max-width、--l-toast-radius、--l-toast-*-icon-size、--l-toast-*-padding 等
