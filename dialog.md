# LimeDialog 对话框

## 介绍

对话框组件，用于重要信息展示与用户反馈。支持标题、内容、确认/取消按钮、自定义插槽；支持组件用法与命令式 `ref.show()` 调用，支持 beforeClose 异步关闭。

**依赖：** `lime-shared`、`lime-style`、`lime-icon`、`lime-button`、`lime-popup`

## 使用

```html
<l-dialog v-model="visible" title="标题" content="内容" confirm-btn="知道了" @confirm="confirm" />
<l-dialog v-model="visible" :cancel-btn="{ content: '取消' }" :confirm-btn="{ content: '确认' }" @confirm="confirm" @cancel="cancel" />
<l-dialog v-model="visible" button-layout="vertical">...</l-dialog>
<l-dialog ref="dialogRef" />
<!-- 命令式：dialogRef.show({ title, content, confirmBtn, cancelBtn, beforeClose }).then(...).catch(...) -->
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / visible | 是否显示 | boolean | false |
| title | 标题 | string | - |
| content | 内容 | string | - |
| actions | 操作栏按钮列表 | object[] | - |
| cancel-btn | 取消按钮：null 不显示；string 文案；Object 透传 Button | string \| Object | - |
| confirm-btn | 确认按钮：同上 | string \| Object | - |
| button-layout | horizontal / vertical | string | horizontal |
| close-btn | 是否显示右上角关闭按钮 | boolean | false |
| close-on-click-overlay | 点击蒙层是否关闭 | boolean | true |
| overlay | 是否显示遮罩 | boolean | true |
| overlay-style | 遮罩样式 | string | - |
| prevent-scroll-through | 防止滚动穿透 | boolean | true |
| z-index | 层级 | number | 888 |
| l-style | 自定义样式 | string | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| confirm | 点击确认 | - |
| cancel | 点击取消 | - |
| action | 点击操作栏按钮 | index: number |
| click | 点击对话框 | event |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 对话框内容 |
| title | 自定义标题 |
| top | 顶部内容 |
| middle | 中间内容 |
| actions | 自定义操作栏 |
| confirm-btn | 自定义确认按钮 |
| cancel-btn | 自定义取消按钮 |

## Ref 方法：show（命令式）

`show(options)` 返回 Promise，resolve 为确认，reject 为取消。参数：title、content、confirmBtn、cancelBtn、buttonLayout、closeOnClickOverlay、beforeClose: (action) => Promise\<boolean\> 等，与 Props 一致。

## 插件标签

- `l-dialog`：组件标签
- `lime-dialog`：演示标签

## 主题定制

--l-dialog-width、--l-dialog-body-max-height、--l-dialog-title-*、--l-dialog-content-*、--l-dialog-close-*、--l-dialog-bg-color、--l-dialog-split-color、--l-dialog-footer-*、--l-dialog-button-*、--l-dialog-border-radius 等，详见官方文档。
