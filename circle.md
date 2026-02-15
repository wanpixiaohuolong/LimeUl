# LimeCircle 环形进度条

## 介绍

环形进度条，用于展示进度、比例。支持 v-model:current 过渡值、自定义大小/线宽/颜色、渐变色、仪表盘模式(dashboard)、缺口(gapDegree/gapPosition)、逆时针(clockwise)、canvas 渲染。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-circle v-model:current="current" :percent="target">
  <text>{{ current }}%</text>
</l-circle>
<l-circle :percent="75" size="150px" :stroke-width="8" stroke-color="#1989fa" trail-color="#ebedf0" />
<l-circle :percent="65" :stroke-color="['#3fecff', '#6149f6']" />
<l-circle :percent="70" dashboard />
<l-circle :percent="60" :gap-degree="60" gap-position="top" />
<l-circle :percent="55" :clockwise="false" />
<l-circle v-model:current="current" :percent="target" canvas />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| percent | 进度百分比 | number | 0 |
| size | 尺寸 | string | 120px |
| lineCap | 线条端点形状 | string | round |
| strokeWidth | 进度环线宽 | number \| string | 6 |
| strokeColor | 进度环颜色，可字符串或数组(渐变) | string \| string[] | - |
| trailWidth | 轨道线宽 | number \| string | 6 |
| trailColor | 轨道颜色 | string | - |
| dashboard | 是否仪表盘样式 | boolean | false |
| clockwise | 是否顺时针 | boolean | true |
| duration | 动画时长(ms) | number | 300 |
| max | 最大值 | number | 100 |
| gapDegree | 缺口角度 | number | 90 |
| gapPosition | 缺口位置 | string | bottom |
| canvas | 是否用 canvas 渲染 | boolean | false |
| canvasId | 自定义 canvas id | string | - |

## Events / Slots

无事件。default 插槽：环形中间内容。

## 插件标签

- `l-circle`：组件标签
- `lime-circle`：演示标签

## 主题定制

--l-circle-trail-*、--l-circle-stroke-*、--l-circle-stroke-cap-*
