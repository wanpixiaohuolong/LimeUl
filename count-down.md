# LimeCountDown 倒计时

## 介绍

倒计时组件，用于展示剩余时间。支持 format 格式、毫秒精度(millisecond)、autoStart、插槽自定义展示、ref.start/pause/reset 手动控制。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-count-down :time="86400000" />
<l-count-down :time="86400000" format="DD天HH小时mm分ss秒" />
<l-count-down :time="86400000" millisecond />
<l-count-down :time="time" @finish="onFinish">
  <template #default="{ hours, minutes, seconds }">...</template>
</l-count-down>
<l-count-down ref="countDown" :auto-start="false" :time="3000" format="ss:SSS" @finish="onFinish" />
<!-- ref: start(), pause(), reset() -->
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| time | 剩余时间(ms) | number | - |
| autoStart | 是否自动开始 | boolean | true |
| format | 显示格式 | string | HH:mm:ss |
| millisecond | 是否毫秒精度 | boolean | - |

## Events 事件

| 名称 | 说明 |
|------|------|
| finish | 倒计时结束 |

## Slots 插槽

| 名称 | 说明 | 参数 |
|------|------|------|
| default | 自定义内容 | timeData（含 hours, minutes, seconds 等） |

## Ref 方法

start()、pause()、reset()

## 插件标签

- `l-count-down`：组件标签

## 主题定制

--l-count-down-text-color、--l-count-down-font-size、--l-count-down-line-height
