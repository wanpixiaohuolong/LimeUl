# LimeTyping 输入中

## 介绍

用于展示「正在输入」状态的组件，常用于聊天、客服、AI 回复等待场景。支持 text 自定义文字、idleDotColor/activeDotColor 圆点颜色。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-typing />
<l-typing text="输入中" />
<l-typing text="思考中" idle-dot-color="#cccccc" active-dot-color="#ff6700" />
<view class="message-received"><l-typing /></view>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| text | 显示文字 | string | 正在输入... |
| idleDotColor | 非激活圆点颜色 | string | - |
| activeDotColor | 激活圆点颜色 | string | - |

## Events / Slots

无事件、无插槽。

## 插件标签

- `l-typing`：组件标签
- `lime-typing`：演示标签

## 主题定制

--l-typing-text-color、--l-typing-bg-color、--l-typing-padding-*、--l-typing-radius、--l-typing-dot-idle-color、--l-typing-dot-active-color
