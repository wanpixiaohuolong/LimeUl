# LimeDateformat 日期格式化

## 介绍

日期格式化展示。支持 date(字符串或时间戳)、format(yyyy/MM/dd hh:mm:ss 等)、locale(zh/en)、threshold 相对时间阈值、refreshRate 自动刷新间隔。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-dateformat date="2024/11/14 05:00" />
<l-dateformat date="1731531854460" />
<l-dateformat date="2024/11/14 05:00" format="yyyy年MM月dd日 hh:mm:ss" />
<l-dateformat date="2024/11/14 05:00" format="MM/dd hh:mm" />
<l-dateformat date="2024/11/14 05:00" :threshold="[60000, 3600000]" />
<l-dateformat date="2024/11/14 05:00" locale="en" />
<l-dateformat date="2024/11/14 05:00" :refresh-rate="60000" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| date | 日期字符串或时间戳 | string | - |
| locale | zh/en | string | zh |
| format | 格式，如 yyyy/MM/dd hh:mm:ss | string | yyyy/MM/dd hh:mm:ss |
| threshold | [毫秒1, 毫秒2] 相对时间阈值 | Array | [0,0] |
| refreshRate | 自动刷新间隔(ms)，0 不刷新 | number | 0 |

## 格式字符

yyyy/yy、MM/M、dd/d、hh/h、mm/m、ss/s。

## 插件标签

- `l-dateformat`：组件标签
- `lime-dateformat`：演示标签

## 主题定制

--l-dateformat-color
