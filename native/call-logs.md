# LimeCallLogs 通讯记录

## 介绍

安卓端获取通话记录、搜索通话录音、监听通话状态的 UTS API，兼容 uniappx。需自定义基座。隐私限制下不一定能搜到录音；仅小米/华为/OPPO/vivo 测试。

**依赖：** 付费插件

## 使用

```js
import { queryCallLogs, onPhoneCallState, offPhoneCallState, isOpenRecord, openRecordSetting, searchRecorderFile } from '@/uni_modules/lime-call-logs'

queryCallLogs({ limit: 10, success(res) { console.log(res) } })
onPhoneCallState((res) => { const state = res.get('state') })  // 0 挂断 1 响铃 2 通话中
offPhoneCallState()
isOpenRecord()   // 是否开启通话录音
openRecordSetting()  // 跳转录音设置
searchRecorderFile({ time: 10000, success(res) {}, fail(err) {} })
```

## API

queryCallLogs(options)：number/name/date/limit、success。onPhoneCallState / offPhoneCallState。isOpenRecord、openRecordSetting。searchRecorderFile(options)：time、success、fail。

## 插件入口

`lime-call-logs`：queryCallLogs、onPhoneCallState、offPhoneCallState、isOpenRecord、openRecordSetting、searchRecorderFile
