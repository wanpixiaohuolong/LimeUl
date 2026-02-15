# LimeChooseFile 文件选择

## 介绍

基于 UTS 的文件选择，参考小程序 chooseFile API。支持安卓、iOS、鸿蒙、H5；可选图片/视频/其他/全部，count、extension(H5)。需自定义基座。

**依赖：** 付费插件

## 使用

```js
import { chooseFile, type ChooseFileOption } from '@/uni_modules/lime-choose-file'

chooseFile({
  filename: 'xxxx',
  type: 'image',
  count: 9,
  success(res) { console.log(res.tempFiles) },
  fail(err) {}
})
```

## API

chooseFile(options)。ChooseFileOption：filename、count、type('video'|'image'|'file'|'all')、extension[]、success、fail、complete。返回 tempFiles[]：name、path、size、time、type。

## 插件入口

`lime-choose-file`：chooseFile
