# LimeNavbar 导航栏

## 介绍

页面顶部导航栏。支持 title、leftArrow、delta 后退层数、titleMaxLength、fixed、placeholder、safeAreaInsetTop、capsule/left/right/title/extra 插槽、bgColor/color、@click-left/@back。

**依赖：** `lime-style`、`lime-shared`、`lime-icon`（lime-svg 可选）

## 使用

```html
<l-navbar title="标题" :fixed="false" />
<l-navbar title="标题" :left-arrow="true" @click-left="onClickLeft" />
<l-navbar title="很长标题" :title-max-length="5" />
<l-navbar><template #capsule>自定义胶囊</template><template #right>右侧</template></l-navbar>
<l-navbar><template #left><l-search placeholder="搜索" shape="round" /></template></l-navbar>
<l-navbar bg-color="#3283ff" color="white" />
<l-navbar><template #extra="{ size }"><l-popup :overlay-style="{ top: size.height + 'px' }" /></template></l-navbar>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| placeholder | 固定时是否占位 | boolean | false |
| safeAreaInsetTop | 顶部安全区 | boolean | false |
| animation | 是否动画 | boolean | true |
| fixed | 是否固定顶部 | boolean | true |
| leftArrow | 是否左侧箭头 | boolean | false |
| title | 标题 | string | - |
| titleMaxLength | 标题最大长度，超出省略 | number | - |
| delta | 后退层数 | number | 1 |
| zIndex | 层级 | number | - |
| bgColor, color | 背景/文本色 | string | - |

## Events 事件

| 名称 | 说明 |
|------|------|
| back | 返回触发 |
| click-left | 点击左侧 |

## Slots 插槽

capsule（左侧胶囊）、left、right、title、extra（额外，如顶部弹窗，参数 { size }）。

## 插件标签

- `l-navbar`：组件标签
- `lime-navbar`：演示标签

## 主题定制

--l-navbar-color、--l-navbar-bg-color、--l-navbar-height、--l-navbar-title-font-*、--l-navbar-left-arrow-size、--l-navbar-capsule-*
