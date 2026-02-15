# LimePopover 气泡弹出框

## 介绍

气泡弹出框，用于在触发元素周围显示提示或菜单。支持 placement(top/left/right/bottom 及 *-left/*-right)、theme(light/dark 或颜色)、showArrow、visible 受控、closeOnClickOutside、color、disabled、content 插槽。小程序可配合 closeOutside() 手动关闭。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-popover content="简单提示"><button>点击显示</button></l-popover>
<l-popover content="顶部" placement="top">...</l-popover>
<l-popover content="暗色" theme="dark" />
<l-popover content="自定义颜色" color="#ff5500" />
<l-popover :show-arrow="false" />
<l-popover :visible="visible"><button @click="toggle">显示/隐藏</button></l-popover>
<l-popover><template #content>自定义内容</template><button>自定义</button></l-popover>
<l-popover :close-on-click-outside="false" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| content | 气泡内容 | string | - |
| placement | top/top-left/top-right/bottom/bottom-left/bottom-right/left/left-top/left-bottom/right/right-top/right-bottom | string | top |
| theme | light/dark 或颜色值 | string | light |
| showArrow | 显示箭头 | boolean | true |
| visible | 是否显示，null 为非受控 | boolean | null |
| closeOnClickOutside | 点击外部关闭 | boolean | true |
| color | 自定义气泡颜色 | string | - |
| disabled | 禁用 | boolean | false |
| scrollPosition | 滚动值(滚动时定位) | number | - |

## Slots 插槽

default：触发元素；content：气泡内容。

## 插件标签

- `l-popover`：组件标签
- `lime-popover`：演示标签

## 主题定制

--l-popover-border-radius、--l-popover-font-size、--l-popover-padding、--l-popover-arrow-size、--l-popover-margin、--l-popover-color、--l-popover-bg-color
