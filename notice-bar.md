# LimeNoticeBar 通知栏

## 介绍

通知栏，用于循环展示消息。支持 text(字符串或数组)、leftIcon/rightIcon、type(info/success/warning/danger)、interval/delay/speed/loop、marquee 水平滚动、vertical 垂直滚动、wrapable 换行、color/bgColor、leftIconColor/rightIconColor、fontSize、@click。

**依赖：** `lime-shared`、`lime-style`、`lime-icon`（lime-svg 在 uniappx 可选）

## 使用

```html
<l-notice-bar text="这是一条通知" />
<l-notice-bar text="通知" left-icon="" />
<l-notice-bar text="通知" right-icon="close" @click="handleClick" />
<l-notice-bar :wrapable="true" text="较长通知多行展示" />
<l-notice-bar :marquee="true" text="水平滚动通知" />
<l-notice-bar :marquee="true" :vertical="true" :text="['第一条','第二条']" />
<l-notice-bar type="success" text="成功" /><l-notice-bar type="warning" text="警示" />
<l-notice-bar bg-color="#3283ff" color="white" left-icon-color="white" />
<l-notice-bar :marquee="true" :speed="100" :interval="3000" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| text | 通知文本或数组 | string \| Array | - |
| leftIcon, rightIcon | 左/右图标名 | string | - |
| type | info/success/warning/danger | string | info |
| interval | 垂直播放间隔(ms) | number | 2000 |
| delay | 动画延迟(ms) | number | 0 |
| speed | 滚动速率(px/s) | number | 50 |
| loop | 循环次数，-1 无限 | number | 2 |
| color, bgColor | 文本/背景色 | string | - |
| marquee | 是否滚动 | boolean | false |
| vertical | 是否垂直播放 | boolean | false |
| wrapable | 是否换行(非滚动时) | boolean | false |
| leftIconColor, leftIconSize, rightIconColor, rightIconSize, fontSize | 样式 | string | - |
| lStyle | 自定义样式 | string \| object | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| click | 点击通知栏 | event: Event |

## Slots 插槽

default、left-icon、right-icon。

## 插件标签

- `l-notice-bar`：组件标签
- `lime-notice-bar`：演示标签

## 主题定制

--l-notice-bar-font-size、--l-notice-bar-padding-*、--l-notice-bar-*-color、--l-notice-bar-*-bg-color（info/success/warning/danger）
