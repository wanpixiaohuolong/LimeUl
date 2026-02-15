# LimePagX PAG 动画播放

## 介绍

基于 PAG 格式的原生动画组件，支持 src 加载、play/pause、load 切换。仅支持安卓、iOS；鸿蒙 Next 需配合 lime-pag。需自定义基座。

**依赖：** 需自定义基座

## 使用

```html
<l-pag-x style="height:300px" :src="pagSrc" ref="pagPlayer" @init="onLoaded" @animationStart="animationStart" @animationEnd="animationEnd" />
```

```js
onLoaded() {
  const player = this.$refs.pagPlayer
  player.play()
}
player.pause()
player.isPlaying()
player.load('/static/new.pag')
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| src | PAG 文件地址 | string | "" |

## Events 事件

init、animationStart、animationEnd、animationUpdate、animationRepeat、animationCancel、frame(frame)、fail(error)。

## Ref 方法

play()、pause()、isPlaying()、load(src)。

## 插件入口

`lime-pag-x`：组件 l-pag-x
