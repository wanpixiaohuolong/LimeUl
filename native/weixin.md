# LimeWeixin 微信功能集成

## 介绍

UTS 集成微信核心功能：登录、分享、跳转小程序、打开 APP 参数等。适用于 Android/iOS，需配置包名/AppID/Universal Link 后自定义基座。

**依赖：** 付费插件；需微信开放平台配置

## 使用

```js
import { useWeiXin, type UseWeiXinOptions } from '@/uni_modules/lime-weixin'

const wxUtils = useWeiXin({
  appId: 'wx...',
  universalLink: 'https://yourdomain.com/universal-link/',
  success(res) {},
  fail(err) {}
})
wxUtils.isInstalled()
wxUtils.openApp()
wxUtils.navigateToMiniProgram({ appId, path, envVersion })
wxUtils.login({ success(res) {} })
wxUtils.launch({ success(res) { console.log(res.extInfo) } })
wxUtils.share({ type: 'image', imageUrl, thumb, scene: 'timeline' })
wxUtils.share({ type: 'webpage', title, summary, webpageUrl, thumb })
wxUtils.share({ type: 'miniProgram', title, miniProgramId, miniProgramPath, thumb })
```

## API

useWeiXin(options)。实例方法：isInstalled、openApp、navigateToMiniProgram、login、launch、share。ShareOptions 按 type(text/image/imageText/webpage/miniProgram/video/music/file) 不同必填参数不同。

## 插件入口

`lime-weixin`：useWeiXin
