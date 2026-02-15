# LimeAudioPlayer 音频播放

## 介绍

参考小程序 createInnerAudioContext 的音频播放 API，用法一致。

**依赖：** 无

## 使用

```js
import { createInnerAudioContext } from '@/uni_modules/lime-audio-player'

const ctx = createInnerAudioContext()
ctx.src = 'xxxx.mp3'
ctx.onCanplay(() => {
  console.log('可以播放')
  ctx.play()
})
ctx.play()
ctx.pause()
```

## API

createInnerAudioContext() 返回与小程序 InnerAudioContext 一致的实例（src、play、pause、onCanplay 等）。详见 createInnerAudioContext 文档。

## 插件入口

`lime-audio-player`：createInnerAudioContext
