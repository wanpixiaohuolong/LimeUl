# LimeSvga SVGA 动画

## 介绍

SVGA 动画组件，兼容 UniApp（微信小程序、H5、安卓、iOS）和 UniAppX（微信小程序、H5、安卓、iOS、鸿蒙）。可直接设 src 播放，或通过 @init 获取 { parser, player } 实现高级控制：parser.load、player.setVideoItem、player.loops、player.startAnimation、player.onFinished 等。H5 需 `npm install svgaplayerweb`；UniAppX App 需 lime-svga-x。需源码运行。

**依赖：** H5 需 svgaplayerweb；UniAppX App 需 lime-svga-x

## 使用

```html
<l-svga src="https://.../angel.svga" style="height:750rpx" />
<l-svga ref="svga" @init="render" />
```

```js
const render = async ({ parser, player }) => {
  const videoItem = await parser.load(url)
  await player.setVideoItem(videoItem)
  player.loops = 1
  player.startAnimation()
  player.onFinished(() => console.log('结束'))
}
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| src | SVGA 地址(网络或本地) | string | - |

## Events 事件

init({ parser, player })。

## Player 实例

loops、clearsAfterStop、fillMode、setVideoItem、setContentMode、startAnimation、startAnimationWithRange、pauseAnimation、stopAnimation、clear、stepToFrame、stepToPercentage、setImage、setText、clearDynamicObjects、onFinished、onFrame、onPercentage。contentMode: Fill/AspectFill/AspectFit。

## 插件标签

- `l-svga`：组件标签
- `lime-svga`：演示标签

## 主题定制

无
