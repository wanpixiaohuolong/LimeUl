# LimeShare 系统分享

## 介绍

调用系统分享面板，可分享文本、图片、视频、文件。兼容 uniappX(安卓、iOS)。

**依赖：** 无；分享文件可用 lime-choose-file

## 使用

```js
import { shareWithSystem } from '@/uni_modules/lime-share'

shareWithSystem({ type: 'text', title: '分享到', summary: '文本内容' })
shareWithSystem({ type: 'image', title: '分享到', path: res.tempFilePaths[0] })
shareWithSystem({ type: 'video', title: '分享到', path: res.tempFilePath })
shareWithSystem({ type: 'file', title: '分享到', path: res.tempFiles[0].path })
```

## API

| 方法 | 说明 |
|------|------|
| shareWithSystem(options) | 调起系统分享，ShareOption：type('text'|'image'|'video'|'file')、title、summary、path |

## 插件入口

`lime-share`：shareWithSystem
