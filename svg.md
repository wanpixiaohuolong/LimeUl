# LimeSvg 矢量图标

## 介绍

基于 UTS 的原生矢量图标插件，支持 uniapp/uniappx。可加载本地、网络、源文本、Base64 的 SVG，支持自定义颜色。支持原生与 webview 两种渲染。

**注意：** 付费插件，需从插件市场导入；uniappx 安卓/iOS 在 HBX4.81 之前需自定义基座。

## 使用

```html
<l-svg style="width: 150rpx;height: 150rpx;" src="/static/svg/a.svg"></l-svg>
<l-svg src="https://example.com/icon.svg" color="red"></l-svg>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| src | SVG 源：本地路径/网络 URL/SVG 源文本/Base64 | string | - |
| color | 图标颜色（仅纯色有效） | string | - |
| web | 是否用 WebView 渲染（支持动画） | boolean | false |
| width | 图标宽度 | string \| number | - |
| height | 图标高度 | string \| number | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| click | event: Event | 点击图标 |
| load | - | 加载完成 |
| error | error: Error | 加载失败 |

## Slots 插槽

无

## 插件标签

- `l-svg`：组件标签
- `lime-svg`：演示标签
