# LimeGzip GZip 解压

## 介绍

GZip 数据流解压。decompressGzip 异步、decompressGzipSync 同步。安卓/iOS 需自定义基座；鸿蒙 Next 和 Web 仅源码。

**依赖：** 无

## 使用

```js
import { decompressGzip, decompressGzipSync, type UnGZipOptions } from '@/uni_modules/lime-gzip'

decompressGzip({
  input: compressedData,  // Uint8Array
  asText: true,
  success(res) { console.log(res.data, res.originalSize, res.compressedSize) }
})
const res = decompressGzipSync({ input: compressedData, asText: false })
```

## API

decompressGzip(options)、decompressGzipSync(options)。UnGZipOptions：input(Uint8Array)、asText。返回 data、outputPath、originalSize、compressedSize。

## 插件入口

`lime-gzip`：decompressGzip、decompressGzipSync
