# LimeLottie Lottie 动画

## 介绍

Lottie 动画组件，兼容 WEB、微信小程序、安卓、iOS、鸿蒙。支持 src 或 frames(JSON)、loop、autoplay、speed、direction(1/-1)；ref.loadAnimation(url)、play、pause、destroy；@loaded 返回 loadAnimation、@ready 返回实例、@complete、@error。小程序/Web 需安装 lottie-miniprogram 或 lottie-web。

**依赖：** `lime-shared`

## 使用

```html
<l-lottie l-style="height:200px" src="https://example.com/animation.json" />
<l-lottie ref="ref" src="..." /><button @click="ref.play()">播放</button>
<l-lottie ref="ref" /><button @click="loadAndPlay">加载并播放</button>
<l-lottie @loaded="onLoaded" />
<l-lottie :loop="true" :autoplay="true" :speed="1.5" />
```

```js
const lottie = await lottieRef.value.loadAnimation('https://...')
lottie.setSpeed(2)
lottie.play()
// ready 事件或 loadAnimation 返回的实例：play/stop/pause/destroy/setSpeed/setDirection/goToAndPlay/goToAndStop/addEventListener/removeEventListener
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| src | 动画资源路径 | string | - |
| frames | 动画 JSON 数据 | Object | - |
| loop | 是否循环 | boolean | false |
| autoplay | 是否自动播放 | boolean | false |
| speed | 播放速度 | number | 1 |
| direction | 1 正向 / -1 反向 | number | 1 |
| lStyle | 自定义样式 | string \| object | - |

## Events 事件

loaded(loadAnimation)、ready(lottie 实例)、complete、error(error)。

## Ref 方法

loadAnimation(url)、play()、pause()、destroy()。

## LimeLottie 实例方法

play、stop、pause、destroy、setSpeed、setDirection、goToAndPlay、goToAndStop、addEventListener、removeEventListener（事件名：loopComplete、complete、segmentStart、destroy）。

## 插件标签

- `l-lottie`：组件标签

## 主题定制

无
