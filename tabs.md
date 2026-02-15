# LimeTabs 选项卡

## 介绍

选项卡，用于内容区切换。支持 list 或 l-tab-panel 子组件；v-model 绑定选中 value；animated、swipeable、spaceEvenly、split、color/activeColor/lineColor/lineWidth/lineHeight/bgColor、size、syncSwiper/swiperProgress 与 swiper 联动、label/left/right 插槽、dot/badge/offset 徽标、@click/@change。兼容 uniapp/uniappx。

**依赖：** `lime-shared`、`lime-badge`、`lime-style`

## 使用

```html
<l-tabs v-model="value" :list="list" />
<l-tabs v-model="activeTab">
  <l-tab-panel :value="0" label="首页" />
  <l-tab-panel :value="1" label="分类" />
  <l-tab-panel :value="2" label="购物车" />
</l-tabs>
<l-tabs :space-evenly="false">...</l-tabs>
<l-tab-panel :value="1" label="联系人" :dot="true" />
<l-tab-panel :value="2" label="通知" badge="8" :offset="[-8,3]" />
<l-tabs :animated="true" :swipeable="true">...</l-tabs>
<l-tabs :value="value" @click="onClick">...</l-tabs>
```

## Tabs Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 当前选中标识 | number | 0 |
| list | 选项卡列表(TabPanelProps[]) | array | [] |
| animated | 切换动画 | boolean | false |
| duration | 动画时长(s)，0 禁用 | number | 0.3 |
| spaceEvenly | 头部是否均分 | boolean | true |
| swipeable | 手势滑动切换 | boolean | false |
| split | 分割线 | boolean | true |
| color, activeColor, lineColor, lineWidth, lineHeight, bgColor | 样式 | string | - |
| size | medium/large 或高度值 | string | - |
| padding | 标题 padding | string | - |
| swiperProgress | 与 swiper 联动进度 [-1,1]，uniappx | number | - |
| syncSwiper | 是否与 swiper 同步，uniappx | boolean | false |
| lStyle, contentStyle | 样式 | string \| Object | - |
| immediate | 跳过首次动画 | boolean | false |

## Tabs Events

| 名称 | 说明 | 回调 |
|------|------|------|
| click | 点击标签 | index: number |
| change | 激活改变 | index: number |

## Tabs Slots

label（{ item, active, disabled }）、left、right、default。

## TabPanel Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| value | 唯一标识 | number | - |
| label | 标签名 | string | - |
| disabled | 禁用 | boolean | false |
| dot | 小红点 | boolean | false |
| badge | 徽标内容 | string \| number | - |
| offset | 徽标偏移 | number[] | [] |

## 插件标签

- `l-tabs`、`l-tab-panel`：组件标签
- `lime-tabs`：演示标签

## 主题定制

--l-tab-font-size、--l-tab-nav-*、--l-tab-content-bg-color、--l-tab-item-*、--l-tab-split-color、--l-tab-track-*
