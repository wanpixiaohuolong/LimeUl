# LimePinyin 汉字转拼音

## 介绍

全端中文转拼音 UTS 库。支持 toneType(symbol/num/none)、pattern(pinyin/initial/final/first/num 等)、type(string/array/all)、multiple 多音字、surname 姓氏模式。可 addDict 自定义词典。App 需自定义基座；建议页面使用 getFileSystemManager 避免打包报错。

**依赖：** 付费插件

## 使用

```js
import { pinyin, addDict, type CompleteOptions } from '@/uni_modules/lime-pinyin'

pinyin('汉语拼音')  // 带音调
pinyin('汉语拼音', { toneType: 'none' })
pinyin('汉语拼音', { toneType: 'num', type: 'array' })
pinyin('汉语拼音', { pattern: 'initial' })
pinyin('好', { multiple: true })
pinyin('我叫曾乐乐', { surname: 'head' })
addDict(dictObj)
```

## API

pinyin(text, options)。CompleteOptions：pattern、toneType、type、multiple、surname。addDict(dict)。

## 插件入口

`lime-pinyin`：pinyin、addDict
