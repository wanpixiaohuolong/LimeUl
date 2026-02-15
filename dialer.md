# LimeDialer 大转盘

## 介绍

转盘抽奖组件，用于营销、活动抽奖。支持 prizeList、size、turns、duration、styleOpt 扇形样式；ref.run(index) 旋转到指定奖项；插槽自定义边框/指针/奖品；@click、@done。

**依赖：** 见官方文档 [Dialer](https://limex.qcoon.cn/components/dialer.html)

## 使用

```html
<l-dialer ref="dialerRef" :prize-list="list" @done="onDone" />
<button @click="dialerRef.run(0)">开始</button>
```

## 插件标签

- `l-dialer`：组件标签
