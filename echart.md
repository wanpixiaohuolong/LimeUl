# LimeEchart 图表

## 介绍

ECharts 图表封装，支持 H5、小程序、App。使用方式：在 @finished 后调用 ref.init(echarts) 得到图表实例，再 setOption。支持 setOption、resize、clear、dispose、showLoading/hideLoading、canvasToTempFilePath。小程序需自行引入 ECharts 构建包(如 require('../../static/echarts.min.js'))。

**依赖：** 无（使用处需 ECharts）

## 使用

```html
<view style="width:750rpx;height:750rpx;">
  <l-echart ref="chartRef" @finished="initChart" />
</view>
```

```js
// #ifdef MP
const echarts = require('../../static/echarts.min.js')
// #endif
// #ifndef MP
const echarts = null
// #endif
const initChart = async () => {
  if (!chartRef.value) return
  const chart = await chartRef.value.init(echarts)
  chart.setOption(option)
}
// 更新: chartRef.value.setOption(newOption) 或 chart.setOption(newOption)
//  resize: chartRef.value.resize() 或 chartRef.value.resize({ width, height })
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| l-style | 自定义样式 | string | - |
| type | canvas 类型(废除) | string | 2d |
| is-disable-scroll | 触摸时禁止页面滚动 | boolean | false |
| beforeDelay | 延迟初始化(ms) | number | 30 |
| enableHover | PC 悬浮(废除) | boolean | false |
| landscape | 旋转 90° 横屏 | boolean | false |
| autoHideTooltip | 自动隐藏 tooltip | boolean | false |

## Events 事件

finished：画布就绪，此时可调用 init。

## Ref 方法

- init(echarts, config?) => Promise&lt;ChartInstance&gt;
- setOption(option)
- resize(size?: { width, height })
- clear()
- dispose()
- showLoading() / hideLoading()
- canvasToTempFilePath(options)

## 插件标签

- `l-echart`：组件标签
- `lime-echart`：演示标签

## 主题定制

无组件级主题变量（使用 ECharts 配置）
