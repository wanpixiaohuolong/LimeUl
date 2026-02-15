# LimeVideoThumb 视频缩略图

## 介绍

获取本地视频封面或指定时间点帧图。需自定义基座。

**依赖：** 无

## 使用

```js
import { getVideoThumb, type GetVideoThumbOptions } from '@/uni_modules/lime-video-thumb'

getVideoThumb({
  path: '/static/video.mp4',
  time: 5000,
  success(coverPath) { console.log(coverPath) },
  fail(err) {}
})
```

## API

getVideoThumb(options)。GetVideoThumbOptions：path、time(ms，默认 0)、success、fail、complete。

## 插件入口

`lime-video-thumb`：getVideoThumb
