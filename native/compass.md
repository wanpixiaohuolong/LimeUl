# LimeCompass 罗盘

## 介绍

参考 uni.onCompassChange 实现的罗盘 UTS API，兼容 uniappx(web、安卓)，iOS 未测。

**依赖：** 无

## 使用

```js
import { onCompassChange, offCompassChange } from '@/uni_modules/lime-compass'

onCompassChange((result) => { console.log(result) })
offCompassChange()
```

## API

| 方法 | 说明 |
|------|------|
| onCompassChange(callback) | 开始监听罗盘 |
| offCompassChange | 取消监听 |

## 插件入口

`lime-compass`：onCompassChange、offCompassChange
