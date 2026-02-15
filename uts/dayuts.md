# LimeDayuts 日期库

## 介绍

轻量日期时间 UTS 库，API 与 dayjs 基本一致。解析、取值/赋值、加减、startOf/endOf、format、比较、diff、fromNow/to、locale。支持格式化占位符 YYYY/MM/DD/HH/mm/ss 等。

**依赖：** 无

## 使用

```js
import { dayuts } from '@/uni_modules/lime-dayuts'

dayuts().format()
dayuts('2024-03-04T16:00:00.000Z').format('DD/MM/YYYY')
dayuts(1318781876406)
dayuts().add(7, 'day').subtract(1, 'year')
dayuts().startOf('year').endOf('month')
dayuts().isBefore(dayuts('2011-01-01'))
dayuts().isAfter(dayuts('2011-01-01'))
dayuts('2010-10-20').isBetween('2010-10-19', dayuts('2010-10-25'))
dayuts().fromNow()
dayuts().diff(dayuts('2020-01-01'), 'day')
```

## API

dayuts()/dayuts(string)/dayuts(string, format)/dayuts(number)/dayuts(Date)/dayuts(array)。取值赋值：millisecond、second、minute、hour、date、day、month、year、get、set。操作：add、subtract、startOf、endOf。显示：format、fromNow、from、toNow、to、diff、valueOf、unix、daysInMonth、toDate、toJSON。查询：isBefore、isAfter、isSame、isSameOrBefore、isSameOrAfter、isBetween、isLeapYear、isToday。locale。

## 插件入口

`lime-dayuts`：dayuts
