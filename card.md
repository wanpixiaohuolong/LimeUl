# LimeCard 卡片

## 介绍

卡片组件，用于内容区块展示。支持标题、副标题、图标、封面图、操作按钮等，适用于图文、产品、新闻等场景。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-card title="卡片标题" note="副标题" extra="更多" more>
  <text>卡片内容</text>
</l-card>
<l-card title="标题" cover="https://..." coverMode="aspectFill" :actions="actions" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| title | 卡片标题 | string | - |
| note | 同行说明文字 | string | - |
| extra | 右侧额外文字 | string | - |
| icon | 左侧图标名称 | string | - |
| image | 左侧图片地址 | string | - |
| cover | 封面图地址 | string | - |
| more | 是否显示更多图标 | boolean | false |
| inset | 是否内嵌样式 | boolean | true |
| actions | 操作按钮列表 | Array | - |
| actionsAlign | 操作对齐 left/right/space-between | string | right |
| iconColor / rightIcon / rightIconColor | 图标相关 | string | - |
| iconSize / rightIconSize | 图标尺寸 | string | - |
| lStyle / imageStyle / coverStyle | 自定义样式 | string \| object | - |
| coverMode | 封面图裁剪模式 | string | widthFix |
| bgColor | 卡片背景色 | string | - |
| headerBordered | 是否头部边框 | boolean | true |
| footerBordered | 是否底部边框 | boolean | true |
| lClass / lClassLeftIcon / lClassRightIcon | 自定义类名 | string | - |

**coverMode 可选值：** scaleToFill、aspectFit、aspectFill、widthFix、heightFix、top、bottom、center、left、right 等

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| action | index: number | 点击操作按钮 |
| more | event: UniEvent | 右侧更多点击 |
| getuserinfo / contact / getphonenumber / error / opensetting / launchapp / chooseavatar / agreeprivacyauthorization | event: UniEvent | 开放能力回调 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 卡片内容 |
| cover | 自定义封面 |
| title | 自定义标题区域 |
| icon | 自定义图标 |
| header-extra | 自定义头部右侧 |
| footer | 自定义底部 |

## Action 按钮配置

与 lime-button 一致，含 content、type、block、disabled、icon、loading、ghost、shape、size、variant、color、textColor、fontSize 等。

## 插件标签

- `l-card`：组件标签
- `lime-card`：演示标签

## 主题定制

提供大量 CSS 变量，如 --l-card-header-line-height、--l-card-bg-color、--l-card-title-color、--l-card-border-radius 等，详见组件文档。
