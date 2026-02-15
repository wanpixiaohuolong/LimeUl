# LimeKeepAlive 应用保活

## 介绍

跨平台保活：Android 前台服务/音乐/一像素/WorkManager/电池白名单/崩溃重启；iOS 后台任务/音频/定时器/网络/本地通知。需先引入再自定义基座。

**依赖：** 付费插件

## 使用

```js
import { useKeepAlive, type UseKeepAliveOptions } from '@/uni_modules/lime-keep-alive'

const keepAlive = useKeepAlive({ success(res) {}, fail(err) {} })
keepAlive.setTitle('我的应用')
keepAlive.setContent('正在后台运行')
keepAlive.addBackgroundCallback((isBackground) => {})
keepAlive.register()
keepAlive.openKeepLive()
keepAlive.unregister()
keepAlive.restart()
// Android: setOnePixEnabled、setWorkerEnabled、setCrashRestartUIEnabled、requestIgnoreBatteryOptimizations 等
// setMusicEnabled、setMusicInterval
```

## API

useKeepAlive(options)。register、unregister、restart、openKeepLive、isDebug、setTitle、setContent、addBackgroundCallback、updateNotification 等。Android 专用：setOnePixEnabled、setWorkerEnabled、requestIgnoreBatteryOptimizations 等。

## 插件入口

`lime-keep-alive`：useKeepAlive
