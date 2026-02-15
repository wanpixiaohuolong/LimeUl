# LimeDailyPunch 打卡签到日历

## 介绍

签到打卡日历，数据驱动。支持自定义已打卡日期(signedDates)、补签(canSupplement)、连续打卡统计、切换月份、自定义样式。兼容 uniapp/uniappx。

**依赖：** `lime-style`、`lime-shared`

## 使用

```html
<l-daily-punch :signedDates="checkIns" @select="select" @panelChange="change" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| canSupplement | 是否支持补签 | boolean | true |
| yearMonth | 显示年月 YYYY-MM | string | 当前月 |
| signedDates | 已打卡日期数组 YYYY-MM-DD[] | string[] | [] |
| dayHeight | 天格子高度 | number | 76 |
| week | 星期文案数组 | string[] | ['周日',...'周六'] |
| weekStartsOn | 每周起始日(6=周一) | number | 6 |
| weekColor / weekFontSize / weekHeight | 星期栏样式 | string/number | - |
| selectedDayBgColor | 选中日背景色 | string | - |
| dayFontSize / textColor / disabledColor | 日期样式 | number/string | - |
| monthTitleHeight / monthTitleFontSize | 年月标题样式 | number | - |
| color | 主色(签到、今日选中) | string | #3B87F6 |
| unsignedColor | 可补签小点颜色 | string | #F1A33A |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| select | day: LimeDailyPunchDay | 点击某日（可区分今日、已签、可补签） |
| streak | - | 统计连续打卡时触发 |
| panelChange | res: LimeDailyPunchYearMonth | 切换月份时触发 |

## Slots 插槽

无

## 插件标签

- `l-daily-punch`：组件标签
- `lime-daily-punch`：演示标签

## 主题定制

--l-daily-punch-month-title-*、--l-daily-punch-arrow-*、--l-daily-punch-week-*、--l-daily-punch-day-*、--l-daily-punch-text-color、--l-daily-punch-color、--l-daily-punch-unsigned-color、--l-daily-punch-selected-bg-color 等。uniappx 基于 canvas 不支持 CSS 变量。
