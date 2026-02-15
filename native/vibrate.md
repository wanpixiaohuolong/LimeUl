# LimeVibrate 震动

## 介绍

基于 UTS 的震动功能，支持安卓、鸿蒙 Next、iOS。安卓可指定时长(ms)，iOS 不支持时长。Web、小程序不支持。

**依赖：** 无

## 使用

```js
import { vibrate } from '@/uni_modules/lime-vibrate'

vibrate()        // 默认约 150ms
vibrate(200)     // 指定 200ms（iOS 无效）
```

## API

| 方法 | 说明 | 参数 |
|------|------|------|
| vibrate | 触发设备震动 | duration?: number（毫秒，iOS 无效） |

## 插件入口

`lime-vibrate`：vibrate
