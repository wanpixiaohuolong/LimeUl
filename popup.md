# LimePopup 弹出层

## 介绍

弹出层容器，用于弹窗、信息提示等。支持多种弹出位置和动画，兼容 uniapp/uniappx。

**依赖：** `lime-style`、`lime-shared`、`lime-overlay`、`lime-transition`、`lime-icon`

## 使用

```html
<l-popup v-model="show" position="bottom">
  <view style="padding: 100px;">内容</view>
</l-popup>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / visible | 是否显示弹出层 | boolean | false |
| overlay | 是否显示遮罩 | boolean | true |
| position | 弹出位置 | string | center |
| transitionName | 内容区动画名 | string | '' |
| duration | 动画时长(ms)，0 禁用 | number | 300 |
| z-index | 层级 | number | 999 |
| preventScrollThrough | 是否锁定背景滚动 | boolean | true |
| closeOnClickOverlay | 点击遮罩是否关闭 | boolean | true |
| safeAreaInsetBottom | 适配底部安全区 | boolean | true |
| safeAreaInsetTop | 适配顶部安全区 | boolean | true |
| destroyOnClose | 关闭后是否销毁 | boolean | false |
| closeable | 是否显示关闭图标 | boolean | false |
| closeIcon | 关闭图标名称或图片链接 | string | cross |
| bgColor | 背景色 | string | - |
| iconColor | 图标色 | string | - |
| lStyle | 自定义样式 | string \| object | - |
| overlayStyle | 遮罩层样式 | string \| object | - |
| radius | 圆角 | string \| number \| Array | - |

**position 可选值：** top、bottom、left、right、center

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| click-overlay | - | 点击遮罩 |
| click-close | - | 点击关闭图标 |
| open | - | 打开时立即触发 |
| close | - | 关闭时立即触发 |
| opened | - | 打开且动画结束 |
| closed | - | 关闭且动画结束 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 弹窗内容 |
| close-btn | 关闭按钮 |

## 插件标签

- `l-popup`：组件标签
- `lime-popup`：演示标签

## 主题定制 CSS 变量

| 变量名 | 默认值 | 描述 |
|--------|--------|------|
| --l-popup-bg-color | #fff | 弹出层背景色 |
| --l-popup-close-icon-color | rgba(0,0,0,0.6) | 关闭图标颜色 |
| --l-popup-border-radius | $border-radius | 弹出层圆角 |
| --l-overlay-bg-color | rgba(0,0,0,0.6) | 遮罩背景与透明度 |
| --l-overlay-blur | 4px | 遮罩模糊程度 |
