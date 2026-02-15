# LimeButton 按钮

## 介绍

功能丰富的按钮组件，支持多种类型、样式、尺寸和状态。用于表单提交、跳转、确认等场景。

**依赖：** `lime-style`、`lime-shared`、`lime-loading`、`lime-icon`

## 使用

```html
<l-button type="primary">品牌色</l-button>
<l-button type="primary" variant="outline" size="large" block>镂空通栏</l-button>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| type | 按钮类型 | string | default |
| variant | 按钮变体 | string | - |
| disabled | 是否禁用 | boolean | false |
| loading | 是否显示加载状态 | boolean | false |
| size | 按钮尺寸 | string | medium |
| shape | 按钮形状 | string | rectangle |
| icon | 图标名称 | string | - |
| iconSize | 图标大小 | string | - |
| block | 是否块级元素 | boolean | false |
| ghost | 是否幽灵按钮 | boolean | false |
| content | 按钮文本内容 | string | - |
| color | 按钮颜色 | string | - |
| radius | 按钮圆角 | string | - |
| fontSize | 文字大小 | string | - |
| textColor | 文字颜色 | string | - |
| formType | 表单提交类型 | string | - |
| openType | 微信开放能力 | string | - |
| gap | 图标与文本间距 | string | - |
| lId | 按钮 ID | string | - |
| lStyle | 自定义样式 | string | - |

**type 可选值：** default、primary、success、warning、danger  
**variant 可选值：** solid、outline、dashed、light、text  
**size 可选值：** mini、small、medium、large  
**shape 可选值：** rectangle、square、round、circle  

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| click | event: Event | 点击按钮 |
| getuserinfo | event: UniEvent | 获取用户信息回调 |
| contact | event: UniEvent | 客服消息回调 |
| getphonenumber | event: UniEvent | 获取手机号回调 |
| error | event: UniEvent | 开放能力错误回调 |
| opensetting | event: UniEvent | 打开授权设置页回调 |
| launchapp | event: UniEvent | 打开 APP 成功回调 |
| chooseavatar | event: UniEvent | 获取用户头像回调 |
| agreeprivacyauthorization | event: UniEvent | 同意隐私协议回调 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 按钮内容 |

## 插件标签

- `l-button`：组件标签
- `lime-button`：演示标签

## 主题定制

组件提供大量 CSS 变量，如 `--l-button-border-radius`、`--l-button-primary-color`、`--l-button-medium-height` 等，详见组件文档主题定制表。
