# LimeClipper 图片裁剪

## 介绍

图片裁剪组件，支持拖动、缩放、旋转。可传入图片路径、固定裁剪框、锁定宽高比、限制移动、禁用缩放/旋转、自定义按钮与工具栏。适用于头像裁剪、图片编辑。uniappx app 基于 canvas，部分 CSS 变量无效。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-clipper v-if="show" @success="onSuccess" @cancel="show = false" />
<l-clipper v-if="show" :image-url="imageUrl" @success="url = $event.url; show = false" @cancel="show = false" />
```

## Props 属性（节选）

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| image-url | 图片路径(相对/临时/本地/网络) | string | - |
| quality | 生成图片质量 0-1 | number | 1 |
| source | 图片来源配置 { album: '从相册选择' } | Object | - |
| fixedBoxWidth | 固定裁剪框宽度(rpx) | number | - |
| width / height | 裁剪框宽高(rpx) | number | 400 |
| min-width / min-height / max-width / max-height | 裁剪框范围 | number | - |
| min-ratio / max-ratio | 图片最小/最大缩放比 | number | 0.5/2 |
| rotate-angle | 旋转按钮每次角度 | number | 90 |
| scale-ratio | 生成图相对裁剪框比例，越高越清晰 | number | 1 |
| is-lock-width / is-lock-height / is-lock-ratio | 锁定宽/高/比例 | boolean | false |
| is-disable-scale / is-disable-rotate | 禁止缩放/旋转 | boolean | false |
| is-limit-move | 限制移动范围 | boolean | false |
| is-show-photo-btn / is-show-rotate-btn | 显示选择图片/旋转按钮 | boolean | true |
| is-show-confirm-btn / is-show-cancel-btn | 显示确定/取消按钮 | boolean | true |
| confirm-bg-color | 确定按钮背景色 | string | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| success | { width, height, url } | 生成图片成功 |
| fail | error | 生成失败 |
| cancel | - | 关闭 |
| ready | { width, height, path, orientation, type } | 图片加载完成 |
| change | { width, height } | 图片大小改变 |
| rotate | angle | 图片旋转时 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| cancel | 取消按钮 |
| photo | 选择图片按钮 |
| rotate | 旋转按钮 |
| confirm | 确定按钮 |
| default | 自定义工具栏等 |

## 插件标签

- `l-clipper`：组件标签
- `lime-clipper`：演示标签

## 主题定制（uniappx app 无效）

--l-clipper-mask-color、--l-clipper-z-index、--l-clipper-confirm-color、--l-clipper-edge-border-width
