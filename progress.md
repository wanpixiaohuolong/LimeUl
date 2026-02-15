# LimeProgress 进度条

## 介绍

线性进度条，支持 percent、showInfo、infoType(outer/inner)、infoAlign(start/end)、strokeColor、trailColor、linecap、infoColor、fontSize、strokeWidth。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-progress :percent="percent" />
<l-progress :percent="percent" :show-info="true" />
<l-progress :percent="percent" info-type="inner" info-align="start" :show-info="true" info-color="white" />
<l-progress :percent="percent" stroke-color="#7232dd" trail-color="..." />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| percent | 进度百分比 | number | 0 |
| showInfo | 是否显示进度信息 | boolean | false |
| infoType | outer / inner | string | outer |
| infoAlign | start / end | string | end |
| strokeColor | 进度条颜色 | string | - |
| trailColor | 背景条颜色 | string | - |
| linecap | 端点形状 | string | - |
| infoColor | 进度信息颜色 | string | - |
| fontSize | 进度信息字号 | string \| number | - |
| strokeWidth | 进度条宽度 | string \| number | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 进度变化 | percent: number |

## 插件标签

- `l-progress`：组件标签
- `lime-progress`：演示标签

## 主题定制

--progress-stroke-*、--progress-trail-*、--progress-border-radius、--progress-duration、--progress-text-color、--progress-inner-text-color
