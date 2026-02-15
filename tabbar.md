# LimeTabbar 标签栏

## 介绍

底部标签栏，用于模块切换。v-model 绑定选中索引或 value；支持 value 匹配、badgeProps 徽标、icon 插槽自定义图标、activeColor/color、fixed/bordered/split/placeholder、shape(round)、theme(tag)、@change。兼容 uniapp/uniappx。

**依赖：** `lime-style`、`lime-shared`、`lime-badge`、`lime-icon`、`lime-svg`

## 使用

```html
<l-tabbar v-model="active">
  <l-tabbar-item icon="home">首页</l-tabbar-item>
  <l-tabbar-item icon="app">应用</l-tabbar-item>
  <l-tabbar-item icon="chat">聊天</l-tabbar-item>
  <l-tabbar-item icon="user">我的</l-tabbar-item>
</l-tabbar>
<l-tabbar v-model="active">
  <l-tabbar-item icon="home" value="home">首页</l-tabbar-item>
  ...
</l-tabbar>
<l-tabbar-item :badge-props="{ content: 16, max: 5 }" />
<l-tabbar-item :badge-props="{ dot: true }" />
<l-tabbar-item><template #icon>自定义图标</template></l-tabbar-item>
<l-tabbar active-color="red" color="#999" />
<l-tabbar v-model="active" @change="change" />
```

## Tabbar Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 当前选中索引或 value | string | - |
| fixed | 是否固定底部 | boolean | true |
| bordered | 是否显示外边框 | boolean | true |
| split | 是否显示分割线 | boolean | false |
| placeholder | 固定时是否占位 | boolean | true |
| zIndex | z-index | number | 885 |
| shape | normal/round | string | normal |
| theme | normal/tag | string | normal |
| safeAreaInsetBottom | 底部安全区 | boolean | true |
| activeColor, color | 选中/未选中颜色 | string | - |
| activeBgColor | 选中背景色 | string | - |
| iconSize, fontSize | 图标/字体大小 | string | - |
| lStyle | 自定义样式 | string | - |

## Tabbar Events

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 切换标签 | active: string |

## TabbarItem Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| value | 匹配标识 | string | - |
| icon | 图标名或图片链接 | string | - |
| disabled | 禁用 | boolean | false |
| label | 文本 | string | '' |
| badgeProps | 徽标属性(透传 Badge) | Object | - |

## TabbarItem Slots

icon、default、extra(文本下方)。

## 插件标签

- `l-tabbar`：组件标签
- `lime-tabbar`：演示标签

## 主题定制

--l-tabbar-bg-color、--l-tabbar-border-color、--l-tabbar-height、--l-tabbar-item-*、--l-tabbar-color、--l-tabbar-active-*、--l-tabbar-disabled-opacity
