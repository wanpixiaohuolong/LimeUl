# LimeBlurView 高斯模糊

## 介绍

高斯模糊视图。APP 下为 UTS 原生实现，非 APP 下使用 CSS backdrop-filter。支持 blur、radius。安卓不宜多层嵌套模糊。

**依赖：** 原生插件（付费）

## 使用

```html
<l-blur-view class="blur" :blur="5">
  <text class="text">高斯模糊</text>
</l-blur-view>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| blur | 模糊强度，越大越模糊 | number | 0 |
| radius | 圆角半径 | number | 0 |

## 插件标签

- `l-blur-view`：组件标签
- `lime-blur-view`：演示标签

## 主题定制

无
