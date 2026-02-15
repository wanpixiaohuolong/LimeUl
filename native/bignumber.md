# LimeBignumber 大数运算

## 介绍

UTS 大数与高精度小数库：加减乘除、取模、幂、比较、舍入、有效位、进制转换、sqrt、shiftedBy 等。兼容 uniapp/uniappx。非源码 APP 需自定义基座；iOS/鸿蒙普通授权需源码版。

**依赖：** 付费插件

## 使用

```js
import { BigNumber } from '@/uni_modules/lime-bignumber'

const a = new BigNumber('0.1')
const b = new BigNumber('0.2')
a.plus(b).toString()
b.minus(a).toString()
b.times(3).toString()
new BigNumber(1).dividedBy(3).toString()
new BigNumber(2).pow(10).toString()
v.isEqualTo('100')
v.comparedTo('100')
num.toString(16)
num.decimalPlaces(2).toString()
num.sd(6).toString()
new BigNumber(16).sqrt().toString()
```

## API

new BigNumber(value, base?)。plus、minus、multipliedBy/times、dividedBy/div、modulo/mod、exponentiatedBy/pow、integerValue、decimalPlaces/dp、sd、precision、shiftedBy、sqrt、comparedTo、isEqualTo/eq、isGreaterThan/gt 等。配置 DECIMAL_PLACES、ROUNDING_MODE 等。

## 插件入口

`lime-bignumber`：BigNumber
