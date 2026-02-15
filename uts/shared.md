# LimeShared 常用函数库

## 介绍

UI 组件开发用轻量工具集：addUnit、camelCase、kebabCase、capitalizedAmount、clamp、closest、fillZero、floatAdd/floatSub/floatMul/floatDiv、getRect/getAllRect、isNumber/isNumeric、random、range、shuffle、sleep、unitConvert、raf/cancelRaf/doubleRaf、exif（不支持 uniappx app）等。

**依赖：** 无

## 使用

```js
import { addUnit } from '@/uni_modules/lime-shared/addUnit'
import { camelCase, kebabCase } from '@/uni_modules/lime-shared/camelCase'
import { clamp, closest } from '@/uni_modules/lime-shared/clamp'
import { fillZero, floatAdd, floatSub, floatMul, floatDiv } from '@/uni_modules/lime-shared/floatAdd'
import { getRect, getAllRect } from '@/uni_modules/lime-shared/getRect'
import { sleep, random, range, shuffle } from '@/uni_modules/lime-shared/sleep'
import { unitConvert } from '@/uni_modules/lime-shared/unitConvert'
import { raf, cancelRaf, doubleRaf } from '@/uni_modules/lime-shared/raf'
import { capitalizedAmount } from '@/uni_modules/lime-shared/capitalizedAmount'

addUnit(100)
camelCase('foo-bar-baz')
clamp(10, 0, 5)
floatAdd(2.1, 3.2)
getRect('#id', this).then(res => {})
sleep(1000)
unitConvert('20px')
```

## API

按模块从 `@/uni_modules/lime-shared/模块名` 引入：addUnit、camelCase、kebabCase、capitalizedAmount、clamp、closest、exif、fillZero、floatAdd、floatDiv、floatMul、floatSub、getRect、getAllRect、isNumber、isNumeric、raf、random、range、shuffle、sleep、unitConvert 等。

## 插件入口

`lime-shared`：各子模块按需引入
