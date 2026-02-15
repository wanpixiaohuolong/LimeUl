# LimeEmpty 空状态

## 介绍

空状态占位组件，内置多种场景图：default、error、cart、404、network、search、comment、order、express、message、coupon、address、developing、maintenance。支持自定义图片 URL、imageSize、description、默认插槽底部内容。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-empty description="空空如也" />
<l-empty image="cart" description="购物车空荡荡" />
<l-empty image="404" description="页面已丢失" />
<l-empty image="https://..." image-size="80" description="描述" />
<l-empty description="描述"><button type="primary">刷新</button></l-empty>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| image | 图片类型或 URL：404, address, cart, comment, coupon, default, developing, error, express, maintenance, message, network, order, search | string | default |
| image-size | 图片大小(px) | number \| string | - |
| description | 描述文字 | string | - |

## Events / Slots

无事件。default 插槽：底部内容。

## 插件标签

- `l-empty`：组件标签

## 主题定制

--l-empty-opacity、--l-empty-padding-*、--l-empty-image-size、--l-empty-description-*
