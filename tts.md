# LimeTts 文本转语音

## 介绍

基于系统原生的 TTS 插件，支持安卓、iOS、鸿蒙。通过 `useTTS()` 创建实例，提供 speak、stop、pause、resume、getVoices、getStatus、destroy；on/off 监听 start、end、error、stop。SpeakOptions 支持 speed、volume、pitch、language、playType、queueMode、person 等。APP 端需自定义基座。

**依赖：** 无（原生能力）

## 使用

```js
import { useTTS } from '@/uni_modules/lime-tts'
const tts = useTTS()
tts.on('start', handleStart)
tts.on('end', handleEnd)
tts.on('error', handleError)
tts.speak('欢迎使用 Lime TTS！')
tts.speak('文本', { speed: 1.2, volume: 1, language: 'zh-CN' })
tts.pause()
tts.resume()
tts.stop()
// 生命周期结束时
tts.off('start', handleStart)
tts.destroy()
```

## useTTS

创建 TTS 实例。

## TTS 实例方法

| 方法 | 说明 |
|------|------|
| speak(text, options?) | 朗读文本，可选 SpeakOptions |
| stop | 停止 |
| pause | 暂停 |
| resume | 恢复 |
| getVoices | 获取可用语音列表 Promise&lt;VoiceInfo[]&gt; |
| getStatus | 获取状态 SpeechStatus |
| destroy | 销毁实例 |
| on(event, callback) | 监听 start/end/error/stop |
| off(event, callback?) | 移除监听 |

## SpeakOptions

speed [0.5-2]、volume [0-2]、pitch [0.5-2]、language ('zh-CN'\|'en-US')、audioType、playType(0 仅合成/1 合成与播报)、soundChannel、queueMode、person。

## 插件标签

非组件，为 API 插件：`lime-tts`，通过 `useTTS` 使用。

## 主题定制

无
