# LimeClipboard 剪贴板

## 介绍

参考小程序 setClipboardData / getClipboardData 的 UTS API，支持 uniappX(web、iOS、安卓)。

**依赖：** 无

## 使用

```js
import { setClipboardData, getClipboardData } from '@/uni_modules/lime-clipboard'

setClipboardData({
  data: '这里是内容',
  success(res) { console.log(res.errMsg) }
})

getClipboardData({
  success(res) { console.log(res.data) }
})
```

## API

| 方法 | 说明 |
|------|------|
| setClipboardData(options) | 写入剪贴板，options.data |
| getClipboardData(options) | 读取剪贴板，success 回调 res.data |

## 插件入口

`lime-clipboard`：setClipboardData、getClipboardData
