# LimeFileUtils 文件与 Base64

## 介绍

文件与 Base64/DataURL 互转的 UTS 工具。APP 为同步返回，非 APP 为 Promise。

**依赖：** 无

## 使用

```js
import { fileToDataURL, fileToBase64, dataURLToFile, processFile } from '@/uni_modules/lime-file-utils'

// APP 同步
url.value = fileToDataURL('/static/logo.png') ?? ''
src.value = dataURLToFile(base64) ?? ''

// 非 APP Promise
fileToDataURL('/static/logo.png').then(res => { url.value = res })
dataURLToFile(base64).then(res => { src.value = res })

processFile({ type: 'toDataURL', path: '/static/logo.png', success: (res) => {} })
processFile({ type: 'toFile', path: base64, filename: 'x', success: (res) => {} })
```

## API

fileToDataURL(filePath)、fileToBase64(filePath)、dataURLToFile(dataURL, filename?)。processFile(options)：type('toBase64'|'toDataURL'|'toFile')、path、filename、success、fail、complete。

## 插件入口

`lime-file-utils`：fileToDataURL、fileToBase64、dataURLToFile、processFile
