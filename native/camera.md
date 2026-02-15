# LimeCamera 相机

## 介绍

参照小程序 camera 组件与 createCameraContext 实现。拍照、录像、闪光灯、前后置、缩放、onCameraFrame。需自定义基座；不支持扫码，扫码可用 lime-scan。试用后再购买。

**依赖：** 付费插件

## 使用

```html
<l-camera style="height:750rpx" @error="onError" :flash="flash" :device-position="device" />
<button @click="takePhoto">拍照</button>
<button @click="startRecord">开始录像</button>
<button @click="stopRecord">结束录像</button>
```

```js
import { createCameraContext } from '@/uni_modules/lime-camera'

const context = createCameraContext()
context.takePhoto({ success(res) { imagePath.value = res.tempImagePath } })
context.setZoom({ zoom: 5, success(res) {} })
context.startRecord({ success() {} })
context.stopRecord({ success(result) { console.log(result.tempThumbPath) } })
const listener = context.onCameraFrame((frame) => { /* frame.data 为 ImageProxy */ })
listener.start()
listener.stop()
```

## Props / 事件

参照小程序 camera：flash、device-position、focus 等；@click。Events：@error。

## API

createCameraContext()：takePhoto、setZoom、startRecord、stopRecord、onCameraFrame（回调中 frame.data 为 ImageProxy）。

## 插件入口

`lime-camera`：组件 l-camera、createCameraContext
