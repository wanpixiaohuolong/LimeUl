# LimeZip 压缩解压

## 介绍

UTS 跨平台压缩解压，支持密码、进度回调。鸿蒙暂不支持密码与进度。

**依赖：** 付费插件，需自定义基座

## 使用

```js
import { zip, type ZipOptions } from '@/uni_modules/lime-zip'
import { unzip, type UnZipOptions } from '@/uni_modules/lime-zip'

zip({
  password: '444555',
  sourcePath: '/static',
  outputPath: '/storage/backup.zip',
  success(res) { console.log(res.tempFilePath) },
  progress(p, t) {}
})
unzip({
  password: '444555',
  zipPath: res.tempFilePath,
  outputPath: '/unpacked',
  success(res) {},
  progress(p, t) {}
})
```

## API

zip(options)：sourcePath/sourcePaths、outputPath、password、success、fail、progress。unzip(options)：zipPath、outputPath、password、success、fail、progress。

## 插件入口

`lime-zip`：zip、unzip
