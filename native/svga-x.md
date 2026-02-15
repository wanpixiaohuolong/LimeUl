# LimeSvgaX SVGA 动画播放器

## 介绍

原生 SVGA 播放组件，支持远程/本地加载、播放/暂停/停止、循环、跳帧/跳百分比、动态替换文本/图片、填充模式。需自定义基座；鸿蒙 Next 需配合 lime-svga 且源码版。

**依赖：** 付费插件

## 使用

```html
<l-svga-x ref="svgaPlayer" src="https://example.com/animation.svga" @loaded="onLoaded" @percentage="onPercentage" />
```

```js
onLoaded() { (this.$refs.svgaPlayer).startAnimation() }
// 动态加载
this.$refs.svgaPlayer.load('https://example.com/new.svga')
// 循环
this.$refs.svgaPlayer.setLoops(0)  // 无限
this.$refs.svgaPlayer.setLoops(3)
// 跳转
this.$refs.svgaPlayer.stepToPercentage(50, true)
this.$refs.svgaPlayer.stepToFrame(10, true)
// 替换
this.$refs.svgaPlayer.setText({ text: '新文本', color: '#FF0000' }, 'textLayer')
this.$refs.svgaPlayer.setImage('/static/new.png', 'imageLayer')
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| src | SVGA 地址(网络/本地) | string | '' |

## Events 事件

init、loaded({url, videoitem})、frame(帧数)、finished、percentage(进度百分比)。

## Ref 方法

load(url)、startAnimation()、pauseAnimation()、stopAnimation()、setLoops(count)、stepToFrame(frame, play)、stepToPercentage(percent, play)、setText(content, key)、setImage(src, key)、setFillMode(mode)、setContentMode(mode)。

## 插件入口

`lime-svga-x`：组件 l-svga-x
