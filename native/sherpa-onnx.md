# LimeSherpaOnnx 实时语音识别

## 介绍

基于 Sherpa-onnx 的本地语音识别，支持音频文件识别与实时录音识别。多种模型类型(paraformer、transducer、whisper、zipformer 等)、online/offline、VAD。支持 Android、iOS。需自定义基座。

**依赖：** 需模型文件（如 paraformer.onnx、silero_vad.onnx、tokens.txt）

## 使用

```js
import { uesSherpaOnnx, type UesSherpaOnnxOptions } from '@/uni_modules/lime-sherpa-onnx'

const recognizer = uesSherpaOnnx({
  model: '/static/models/paraformer.onnx',
  vad: '/static/models/silero_vad.onnx',
  tokens: '/static/models/tokens.txt',
  modelType: 'paraformer',
  mode: 'offline',
  success() {},
  fail(err) {}
})
recognizer.recognizeFile({ audioPath: '/static/test.wav', success(res) { console.log(res.text) } })
recognizer.onRecorder((res) => { console.log(res.text) })
recognizer.startRecorder({ success() {} })
recognizer.stopRecorder()
recognizer.offRecorder()
recognizer.dispose()
```

## API

uesSherpaOnnx(options) 返回识别器。识别器：recognizeFile、onRecorder、offRecorder、startRecorder、stopRecorder、dispose。选项含 model/encoder/decoder/joiner、tokens、vad、modelType、mode、enableVad 等。

## 插件入口

`lime-sherpa-onnx`：uesSherpaOnnx
