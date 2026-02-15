# LimeAvatar 头像

## 介绍

头像组件，支持图片(src)、文字、图标(icon)、形状(circle/square)、尺寸(small/medium/large 或具体值)。l-avatar-group 支持 max、cascading(left-up/right-up)、collapseText、collapseColor 等。

**依赖：** `lime-shared`、`lime-style`（lime-svg 可选）

## 使用

```html
<l-avatar src="https://..." />
<l-avatar shape="square" src="https://..." />
<l-avatar size="small" /><l-avatar size="48px" />
<l-avatar icon="user" />
<l-avatar>A</l-avatar>
<l-avatar color="#1989fa" text-color="#fff">A</l-avatar>
<l-avatar-group>
  <l-avatar src="..." /><l-avatar src="..." />
</l-avatar-group>
<l-avatar-group :max="5" collapse-text="更多" cascading="left-up">...</l-avatar-group>
```

## Avatar Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| size | small/medium/large 或 24px | string | medium |
| shape | circle/square | string | circle |
| src | 图片地址 | string | - |
| icon | 图标名 | string | - |
| fontSize, color, textColor | 样式 | string | - |

## AvatarGroup Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| cascading | left-up/right-up | string | right-up |
| max | 最多显示数量 | number | - |
| shape, size | 同 Avatar | string | - |
| collapseText, collapseFontSize, collapseColor, collapseTextColor | 折叠项 | string | - |

## Slots

Avatar：default（文字或自定义）。AvatarGroup：default（多个 l-avatar）。

## 插件标签

- `l-avatar`、`l-avatar-group`：组件标签
- `lime-avatar`：演示标签

## 主题定制

--l-avatar-bg-color、--l-avatar-text-color、--l-avatar-*-size、--l-avatar-*-font-size、--l-avatar-border-*、--l-avatar-group-overlapping
