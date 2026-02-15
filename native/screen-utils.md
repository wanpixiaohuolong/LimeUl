# LimeScreenUtils 屏幕亮度

## 介绍

参考小程序屏幕亮度 API 实现的 UTS 插件，目前仅安卓端。提供获取/设置屏幕亮度、保持常亮。

**依赖：** 无

## 使用

```js
import { getScreenBrightness, setScreenBrightness, setKeepScreenOn } from '@/uni_modules/lime-screen-utils'

getScreenBrightness({ success(res) { console.log(res.value) } })
setScreenBrightness({ value: 0.5, success(res) {} })
setKeepScreenOn({ keepScreenOn: true, success(res) {}, fail(err) {} })
```

## API

| 方法 | 说明 |
|------|------|
| getScreenBrightness(options) | 获取屏幕亮度，success 回调 res.value |
| setScreenBrightness(options) | 设置亮度，options.value [0-1] |
| setKeepScreenOn(options) | 保持常亮，options.keepScreenOn true/false |

## 插件入口

`lime-screen-utils`：getScreenBrightness、setScreenBrightness、setKeepScreenOn
