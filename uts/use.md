# LimeUse 组合式函数

## 介绍

Vue 组合式函数库。当前提供 useCodeTimer：验证码倒计时，支持开始/重置/停止/暂停/继续、状态持久化(keepRunning + uniqueKey)、onStart/onEnd 回调。

**依赖：** 无

## 使用

```js
import { useCodeTimer } from '@/uni_modules/lime-use'

const {
  tip,
  canGetCode,
  start,
  reset,
  stop,
  pause,
  resume,
  isPaused,
  secondsRemaining
} = useCodeTimer({
  seconds: 120,
  startText: '获取验证码',
  changeText: '重新获取 (X秒)',
  endText: '重新获取',
  keepRunning: true,
  uniqueKey: 'myCodeTimer',
  interval: 1000,
  onStart: () => {},
  onEnd: () => {}
})

const handleGetCode = () => { start() }
```

## useCodeTimer 选项

seconds、startText、changeText、endText、keepRunning、uniqueKey、interval、onStart、onEnd。

## 返回值

tip、canGetCode、start、reset、stop、pause、resume、isPaused、secondsRemaining。

## 插件入口

`lime-use`：useCodeTimer
