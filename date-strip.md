# LimeDateStrip 日期横条

## 介绍

周日历或一组日历横条，支持 v-model 绑定选中日期、按周(swiper)或平铺(switchMode=none)、形状(circle/square/none)、自定义样式与 format 格式化每日文案。

**依赖：** `lime-style`、`lime-shared`

## 使用

```html
<l-date-strip v-model="value" @change="onChange" />
<l-date-strip switchMode="none" :minDate="minDate" :maxDate="maxDate" />
<l-date-strip shape="circle" :format="customFormat" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value / defaultValue | 选中日期(时间戳) | number | - |
| switchMode | none 平铺 / week 按周切换 | string | week |
| shape | 选中框 square/circle/none | string | square |
| minDate / maxDate | 可选最小/最大日期(时间戳) | number | -/当前+31天 |
| height / gridWidth | 组件高度/每格宽度(none 时) | string | - |
| activeBgColor / activeColor | 选中背景色/文本色 | string | - |
| bgColor / radius | 横条背景与圆角 | string | - |
| firstDayOfWeek | 每周第一天 0-6(0=周日) | number | 0 |
| format | 日期格式化 (day)=>day，可改 prefix/suffix 等 | Function | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change / select | time: number | 点击日期时触发 |

## Ref 方法（Expose）

| 名称 | 参数 | 说明 |
|------|------|------|
| scrollToDate | date: Date | 跳转到指定日期 |
| goToPrevWeek | - | 上一周（switchMode=week） |
| goToNextWeek | - | 下一周（switchMode=week） |

## 插件标签

- `l-date-strip`：组件标签
- `lime-date-strip`：演示标签

## 主题定制 CSS 变量

--l-date-strip-bg-color、--l-date-strip-height、--l-date-strip-font-size、--l-date-strip-color、--l-date-strip-active-color、--l-date-strip-prefix/suffix-*、--l-date-strip-grid-*、--l-date-strip-square-radius、--l-date-strip-grid-circle-radius 等。
