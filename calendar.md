# LimeCalendar 日历

## 介绍

日历组件，支持单选、多选(multiple)、区间选择(range)。可搭配弹层或使用 l-calendar-view 无弹层。支持 switchMode( none/month/year-month)、自定义范围、format 格式化日期、maxRange、firstDayOfWeek、预设颜色等。适用于预约、签到、行程。**付费组件。**

**依赖：** `lime-shared`、`lime-style`（lime-svg 可选）

## 使用

```html
<l-calendar v-model:visible="visible" @confirm="handleConfirm" />
<l-calendar v-model:visible="visible" type="range" confirm-btn="确认" />
<l-calendar-view type="range" confirm-btn="确认" />
```

## Props 属性（节选）

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model:visible | 是否显示(usePopup 时) | boolean | false |
| value / v-model | 选中日期(时间戳)，多选/区间为数组 | number \| number[] | - |
| type | single/multiple/range | string | single |
| switchMode | none/month/year-month | string | month |
| minDate / maxDate | 最小/最大可选日期(时间戳) | number | - |
| maxRange | 区间最大天数 | number | - |
| firstDayOfWeek | 每周第一天 0-6 | number | 0 |
| confirmBtn | 确认按钮：null 不显示；string 文案；Object 透传 Button | string \| Object | null |
| confirmDisabledText | 确认按钮禁用时文案 | string | - |
| title | 标题 | string | - |
| format | 日期格式化 (day)=>day | Function | - |
| color | 主题色 | string | - |
| rowHeight / bgColor | 行高/背景色 | string | - |
| showMark | 是否显示月份水印 | boolean | false |
| readonly / fullFillDates | 只读/补全前后月格子 | boolean | false |
| allowCancel | 单选时可取消选中 | boolean | false |
| forceEnableConfirm | 强制启用确认按钮 | boolean | false |
| rangePrompt | 范围选择提示 | string | - |
| localeText | 国际化文案 | Object | - |
| zIndex | 层级 | number | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| select | value: number \| number[] \| null | 点击选中日期时 |
| confirm | value | 点击确认后 |
| change | value | 无 confirm 时选择完成触发(暂不支持 multiple) |
| close | - | 关闭时 |
| panel-change | { date: Date } | 切换年月时(switchMode≠none) |

## Slots 插槽

| 名称 | 说明 | 参数 |
|------|------|------|
| default | 自定义日历内容 | - |
| title | 自定义标题 | - |
| footer | 自定义底部 | - |
| day | 自定义日期格 | day: LDate |

## Ref 方法

| 名称 | 参数 | 说明 |
|------|------|------|
| scrollToDate | date: Date | 滚动到指定日期 |

## LDate 类型

date, day, type, className?, prefix?, prefixStyle?, textStyle?, suffix?, suffixStyle?。type: 'selected'|'middle'|'disabled'|'start'|'centre'|'end'|''。

## 插件标签

- `l-calendar`、`l-calendar-view`：组件标签
- `lime-calendar`：演示标签

## 主题定制

--l-calendar-radius、--l-calendar-bg-color、--l-calendar-active-color、--l-calendar-title-*、--l-calendar-days-*、--l-calendar-item-*、--l-calendar-month-*、--l-calendar-header-border-color 等，详见组件文档。
