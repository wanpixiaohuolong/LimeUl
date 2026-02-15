# LimeSkeleton 骨架屏

## 介绍

加载占位骨架屏，loading 为 true 显示骨架，false 显示子内容。支持 type(avatar/image/text/paragraph/grid/image-list)、animation(gradient/flashed/none)、rowCol 自定义行列、preset 预设(grid/image-list)、rows 重复行数。**付费组件。**

**依赖：** `lime-style`、`lime-shared`

## 使用

```html
<l-skeleton type="avatar" loading />
<l-skeleton type="image" loading animation="flashed" />
<l-skeleton type="paragraph" loading animation="flashed" />
<l-skeleton loading type="grid" :preset="{ columns: 3, rows: 2 }" />
<l-skeleton loading type="image-list" :preset="{ imageWidth: '64px', imageHeight: '64px', textLineCount: 3 }" />
<l-skeleton :loading="isLoading" type="image-list">
  <view class="content-item">真实内容</view>
</l-skeleton>
<l-skeleton loading :row-col="[{ width: '30%', height: '40px' }, { width: '66%', height: '40px' }, ...]" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| loading | 是否加载中（true 显示骨架） | boolean | true |
| animation | gradient / flashed / none（uniappx app 仅 flashed） | string | none |
| delay | 延迟显示(ms) | number | 0 |
| type | avatar / image / text / paragraph / grid / image-list | string | text |
| rowCol | 自定义行列布局，支持嵌套 children | array | - |
| preset | grid/image-list 的预设配置 | object | - |
| rows | 重复 rowCol 次数 | number | - |

## preset（grid）

columns、rows、imageWidth、imageHeight、imageBorderRadius、textWidth、textLineCount、gap 等。

## preset（image-list）

imageWidth、imageHeight、imageBorderRadius、textHeight、textLineCount、gap、rows 等。

## Events / Slots

无常用事件；默认插槽为加载完成后的内容。

## 插件标签

- `l-skeleton`：组件标签
- `lime-skeleton`：演示标签

## 主题定制

--l-skeleton-text-height、--l-skeleton-text-border-radius、--l-skeleton-bg-color、--l-skeleton-rect-border-radius、--l-skeleton-gradient-animation-duration、--l-skeleton-flashed-animation-duration
