# LimeConfetti 彩纸特效

## 介绍

彩纸粒子动画组件，用于庆典、成功反馈等。通过 ref.play(options) 播放；支持 particleCount、angle、spread、colors、shapes(square/circle/star)、origin、scalar、gravity、ticks 等；@done 播放完成。App 可加 renderjs 提升性能；uniappx 需导入 ConfettiOptions 类型。

**依赖：** 无

## 使用

```html
<view style="height:750rpx">
  <l-confetti ref="confettiRef" @done="done" />
</view>
<button @click="run">播放</button>
```

```js
confettiRef.value.play({
  particleCount: 100,
  spread: 70,
  shapes: ['circle'],
  origin: { y: 0.6 }
})
// 多形状
confettiRef.value.play({ shapes: ['square', 'circle', 'star'], ... })
// 自定义颜色
confettiRef.value.play({ colors: ['#ff0000', '#00ff00', '#0000ff'], ... })
```

## Props 属性

无常用 props（主要为容器高度）。

## Events 事件

| 名称 | 说明 |
|------|------|
| done | 动画播放完成 |

## Ref 方法

play(options: ConfettiOptions)

## ConfettiOptions 配置

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| particleCount | 粒子数量 | number | 50 |
| angle | 发射角度(度) | number | 90 |
| spread | 发散角度(度) | number | 45 |
| startVelocity | 初始速度 | number | 45 |
| decay | 速度衰减 | number | 0.9 |
| gravity | 重力 | number | 1 |
| drift | 水平漂移 | number | 0 |
| ticks | 动画帧数 | number | 200 |
| origin | 发射位置 { x, y } 0–1 | object | { x: 0.5, y: 0.5 } |
| colors | 颜色数组(十六进制) | string[] | 默认多色 |
| shapes | square/circle/star | string[] | ['square','circle'] |
| scalar | 大小缩放 | number | 1 |

## 插件标签

- `l-confetti`：组件标签
- `lime-confetti`：演示标签

## 主题定制

无
