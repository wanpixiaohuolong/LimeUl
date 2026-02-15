# LimeBackTop 回到顶部

## 介绍

回到顶部按钮。支持 icon、text、shape(circle/square)、offset 滚动多少后显示、bottom/right 位置、duration、scrollTop(小程序等需传入)、target(nvue/uvue 指定容器)、fixed、@click。

**依赖：** `lime-shared`、`lime-style`、`lime-icon`（lime-svg 可选）

## 使用

```html
<l-back-top />
<l-back-top text="顶部" />
<l-back-top icon="arrow-up" />
<l-back-top shape="circle" /><l-back-top shape="square" />
<l-back-top :offset="300" />
<l-back-top :bottom="100" :right="30" />
<!-- 小程序：根节点或传 scrollTop -->
<l-back-top :scroll-top="scrollTop" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| fixed | 是否固定右下 | boolean | true |
| icon | 图标名，false 不显示 | string \| boolean | 'backtop' |
| iconSize | 图标大小 | string | - |
| text | 按钮文本 | string | - |
| bottom, right | 距底/距右距离 | number \| string | - |
| duration | 回到顶部时长(ms)，nvue 无效 | number | 100 |
| scrollTop | 页面滚动距离(非根节点时传入) | number | 0 |
| offset | 滚动多高后显示，nvue 无效 | number | 200 |
| target | nvue 滚动目标；uvue 容器 ID | string | - |
| shape | circle/square | string | circle |
| lStyle | 自定义样式 | string | - |

## Events 事件

| 名称 | 说明 |
|------|------|
| click | 点击按钮 |

## 插件标签

- `l-back-top`：组件标签
- `lime-back-top`：演示标签

## 主题定制

--l-back-top-font-size、--l-back-top-icon-size、--l-back-top-text-color、--l-back-top-bg-color、--l-back-top-size、--l-back-top-border-*、--l-back-top-position-*、--l-back-top-z-index
