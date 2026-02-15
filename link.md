# LimeLink 超链接

## 介绍

超链接组件，支持应用内跳转；在 APP 端可打开外部浏览器、拨号等。多种样式与尺寸。

**依赖：** `lime-style`、`lime-call`、`lime-shared`、`lime-icon`

## 使用

```html
<l-link type="primary" url="/pages/test/index">内部跳转</l-link>
<l-link href="https://www.example.com">外部跳转</l-link>
<l-link href="tel://177xxxxxx">拨号</l-link>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| url | 应用内跳转链接 | string | - |
| href | 应用外跳转链接 | string | - |
| openType | 应用内跳转方式 | string | navigate |
| prefixIcon | 左侧图标 | string | - |
| suffixIcon | 右侧图标 | string | - |
| type | 主题：primary/info/success/warning/danger/default | string | default |
| disabled | 是否禁用 | boolean | false |
| underline | 是否下划线 | boolean | false |
| size | 尺寸 small/medium/large 或具体值 | string | medium |
| content | 链接内容 | string | - |
| color | 自定义颜色 | string | - |
| navigatorProps | 与 navigator 原生属性一致 | Object | - |

**openType 可选值：** navigate/redirect/switchTab/reLaunch/navigateBack/exit

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| click | event: Event | 点击链接 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 链接内容 |
| prefix | 前置内容 |
| suffix | 后置内容 |

## 插件标签

- `l-link`：组件标签
- `lime-link`：演示标签

## 主题定制 CSS 变量（uvue app 无效）

| 变量名 | 默认值 | 描述 |
|--------|--------|------|
| --l-link-default-color | $text-color-1 | 默认链接颜色 |
| --l-link-primary-color | $primary-color | 主要链接颜色 |
| --l-link-success-color | $success-color | 成功链接颜色 |
| --l-link-warning-color | $warning-color | 警告链接颜色 |
| --l-link-danger-color | $error-color | 危险链接颜色 |
| --l-link-info-color | $info-color | 信息链接颜色 |
| --l-link-icon-size | 28rpx | 图标大小 |
| --l-link-font-size | $font-size | 字体大小 |
