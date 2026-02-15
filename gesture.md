# LimeGesture 手势库

## 介绍

手势处理库，支持旋转、缩放、单指/双指拖拽、滑动、单击、双击、长按等。通过 useGesture(ref, options) 使用，options 含 onRotate、onPinch、onPressMove、onTwoPressMove、onSwipe、onTap、onDoubleTap、onLongTap 等。手动模式可传 ref 为 null，再在 touchstart/touchmove/touchend 中调用 gesture.start/move/end。UniApp 仅源码运行；UniAppX 安卓/iOS 可自定义基座。

**依赖：** 见官方文档

## 使用

```js
import { useGesture, type GestureOptions } from '@/uni_modules/lime-gesture'

const gesture = useGesture(boxRef, {
  onPinch(zoom, evt) { scale.value = Math.min(Math.max(zoom, 0.5), 5) },
  onRotate(angle, evt) { rotation.value += angle },
  onPressMove(delta, evt) { translateX.value += delta.deltaX; translateY.value += delta.deltaY },
  onTwoPressMove(delta, evt) { ... }
})
// 手动模式
gesture.start(e)
gesture.move(e)
gesture.end(e)
gesture.cancel(e)
```

## GestureOptions 回调

onRotate(angle, evt)、onPinch(scale, evt)、onSwipe(direction, evt)、onTap、onDoubleTap、onLongTap、onSingleTap、onPressMove(delta, evt)、onTwoPressMove(delta, evt)、onTouchStart/onTouchMove/onTouchEnd/onTouchCancel、onMultipointStart/onMultipointEnd。

## 方法（手动模式）

start(evt)、move(evt)、end(evt)、cancel(evt)。

## 插件标签

- `l-gesture`：组件标签
- `lime-gesture`：演示标签

## 主题定制

无
