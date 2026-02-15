# LimeXhsshare 小红书集成

## 介绍

UTS 集成小红书分享(图片/视频)、打开活动页、检查是否安装。Android/iOS，需配置包名/AppKey/Universal Link 后自定义基座。

**依赖：** 付费插件

## 使用

```js
import { useXhsShare, type LimeXhsShareConfig } from '@/uni_modules/lime-xhsshare'

const xhsUtils = useXhsShare({
  appKey: '...',
  universalLink: 'https://yourdomain.com/...',
  success(res) {},
  fail(err) {}
})
xhsUtils.isInstalled()
xhsUtils.openUrl('https://www.xiaohongshu.com/activity-page')
xhsUtils.share({ type: 'image', imageUrl, thumb, title, summary })
xhsUtils.share({ type: 'video', title, summary, videoUrl, thumb })
```

## API

useXhsShare(options)。实例：isInstalled、openUrl、share。LimeXhsShareOptions：type('image'|'video')、title、summary、thumb、imageUrl/videoUrl、success、fail、complete。

## 插件入口

`lime-xhsshare`：useXhsShare
