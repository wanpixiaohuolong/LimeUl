# LimeResize 监听元素尺寸变化

## 介绍

当包裹的文档流或所在文档流尺寸变化时触发 resize 事件，用于 DOM 更新后重新获取尺寸与位置并做展示计算。

**依赖：** `lime-shared`

## 使用

```html
<!-- 监听父级：父设 position:relative -->
<view class="parent" style="position: relative;">
  <l-resize @resize="handleResize"></l-resize>
</view>

<!-- 监听子级：包裹要监听的元素，勿给组件加外部样式 -->
<l-resize @resize="handleResize">
  <view class="child"></view>
</l-resize>
```

## Props 属性

无

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| resize | event.detail = { width, height, top, right, bottom, left } | 尺寸变化时触发 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 需要监听尺寸变化的内容 |

## 插件标签

- `l-resize`：组件标签
- `lime-resize`：演示标签
