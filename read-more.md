# LimeReadMore 阅读更多

## 介绍

长文本展开/收起。支持 v-model 控制展开、disabled、expandText/collapseText、expandIcon/collapseIcon、height 收起高度、fontSize/textColor、maskColor 遮罩渐变、@change/@click。

**依赖：** `lime-icon`、`lime-shared`、`lime-style`（lime-svg 在 uniappx 为原生可选）

## 使用

```html
<l-read-more>
  <view><text>长文本内容...</text></view>
</l-read-more>
<l-read-more expand-text="查看全文" collapse-text="收起内容" />
<l-read-more expand-icon="arrow-down" collapse-icon="arrow-up" />
<l-read-more height="150px" />
<l-read-more text-color="#1989fa" font-size="16px" />
<l-read-more :mask-color="['#fff','rgba(255,255,255,0.5)']" />
<l-read-more v-model="isExpanded" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| modelValue / value | 是否展开 | boolean | false |
| disabled | 禁用展开/收起 | boolean | false |
| expandText | 展开按钮文字 | string | 展开更多 |
| expandIcon | 展开图标 | string | chevron-down |
| collapseText | 收起按钮文字 | string | 收起 |
| collapseIcon | 收起图标 | string | chevron-up |
| height | 收起时高度 | string | 100px |
| fontSize, textColor | 按钮样式 | string | - |
| maskColor | 遮罩渐变颜色数组 | Array | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 展开/收起变化 | value: boolean |
| click | 点击展开/收起按钮 | - |

## Slots 插槽

default：需展示的长文本内容。

## 插件标签

- `l-read-more`：组件标签
- `lime-read-more`：演示标签

## 主题定制

--l-read-more-handle-color、--l-read-more-handle-*、--l-read-more-read-start/end、--l-read-more-font-size、--l-read-more-icon-size
