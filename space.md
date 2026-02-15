# LimeSpace 间距

## 介绍

布局组件，在水平或垂直方向为子元素提供均匀间距。非 uvue 端使用 flex gap，可能存在兼容差异。

## 使用

```html
<l-space>
  <l-button type="primary">按钮1</l-button>
  <l-button type="primary">按钮2</l-button>
</l-space>
<l-space direction="vertical" :fill="true" :size="20">
  <l-button block>按钮1</l-button>
  <l-button block>按钮2</l-button>
</l-space>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| direction | 间距方向 vertical / horizontal | string | horizontal |
| size | 间距大小，如 20、20rpx、[20,20] | number \| string \| number[] \| string[] | 8 |
| align | 子元素对齐 start/end/center/baseline | string | - |
| wrap | 是否自动换行（水平时） | boolean | false |
| fill | 是否块级填满父元素 | boolean | false |

## Events 事件

无

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 间距组件内容 |

## 插件标签

- `l-space`：组件标签
- `lime-space`：演示标签
