# LimePag PAG 动画

## 介绍

PAG 动画组件，基于腾讯 PAG 库。兼容 UniApp（微信小程序、H5）和 UniAppX（微信小程序、H5、安卓、iOS、鸿蒙）。通过 @init 回调获得 PAG 对象，使用 PAG.PAGFile.load、PAG.PAGView.init 加载并播放；pagView.play/pause、addListener。UniAppX App 需依赖 lime-pag-x；微信小程序需 `npm install libpag-miniprogram`。小程序本地 .pag 可改后缀 .png 读取。

**依赖：** 微信小程序需 libpag-miniprogram；UniAppX App 需 lime-pag-x

## 使用

```html
<l-pag ref="pagRef" @init="init" />
```

```js
let pagView = null
const init = async (PAG) => {
  const pagFile = await PAG.PAGFile.load('https://pag.art/file/like.pag')
  pagView = await PAG.PAGView.init(pagFile)
  pagView.play()
  pagView.addListener('onAnimationStart', () => {})
  pagView.addListener('onAnimationEnd', () => {})
}
const play = () => { pagView?.play() }
const pause = () => { pagView?.pause() }
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| lStyle | 自定义样式 | string | - |
| src | PAG 文件路径 | string | - |

## Events 事件

init(PAG)、frame(progress)、fail(error)。

## 插件标签

- `l-pag`：组件标签
- `lime-pag`：演示标签

## 主题定制

无
