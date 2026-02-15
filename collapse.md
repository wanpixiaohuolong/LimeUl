# LimeCollapse 折叠面板

## 介绍

折叠面板，用于分组展示内容。由 l-collapse + l-collapse-panel 组成。支持 v-model 控制展开项、手风琴(accordion)、圆角卡片(inset)、图标/图片、禁用、ref.toggleAll(open)。

**依赖：** `lime-shared`、`lime-style`（lime-svg 可选）

## 使用

```html
<l-collapse v-model="activeNames">
  <l-collapse-panel title="标题1" value="1">内容</l-collapse-panel>
  <l-collapse-panel title="标题2" value="2">内容</l-collapse-panel>
</l-collapse>
<l-collapse accordion>...</l-collapse>
<l-collapse inset>...</l-collapse>
<l-collapse-panel title="标题" icon="home" icon-color="#1989fa" />
<l-collapse-panel image="..." image-width="40px" image-height="40px" />
<l-collapse ref="ref" /><button @click="ref.toggleAll(true)">全部展开</button>
```

## Collapse Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / modelValue / value | 展开的面板 value 数组 | array | [] |
| inset | 是否圆角卡片风格 | boolean | false |
| accordion | 手风琴(仅展一个) | boolean | false |
| disabled | 禁用所有面板 | boolean | false |

## CollapsePanel Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| title | 标题 | string | - |
| value | 唯一标识，空则用下标 | string \| number | - |
| disabled | 禁用 | boolean | false |
| icon / image | 左侧图标/图片 | string | - |
| note | 标题同行说明 | string | - |
| size | small/medium/large | string | medium |
| iconColor, iconSize, rightIconColor, rightIconSize | 图标样式 | string | - |
| imageWidth, imageHeight | 图片宽高 | string | - |
| bgColor | 面板背景色 | string | - |

## Collapse Events

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 点击展开/收起 | event: string |

## Collapse Slots

default：一组 l-collapse-panel。

## CollapsePanel Slots

default、title、note、description、icon、rightIcon。

## Ref 方法

toggleAll(open: boolean) 全部展开/全部切换。

## 插件标签

- `l-collapse`、`l-collapse-panel`：组件标签
- `lime-collapse`：演示标签

## 主题定制

--l-collapse-inset-*、--l-collapse-panel-bg-color、--l-collapse-content-*、--l-collapse-right-icon-*、--l-collapse-border-color
