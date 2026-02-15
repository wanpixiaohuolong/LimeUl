# LimeSegmented 分段器

## 介绍

分段器，用于多选项切换。v-model 绑定选中索引；options 数组；shape(round)、type(button/card/text)、size(small/medium/large)、color/activeColor/bgColor/sliderColor、disabled、immediate 跳过首次动画、@change/@click。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-segmented v-model="value" :options="options" />
<l-segmented shape="round" />
<l-segmented v-model="value" type="button" /><l-segmented type="text" />
<l-segmented size="small" /><l-segmented size="large" />
<l-segmented color="#34c471" active-color="#fff" bg-color="#f3fff8" slider-color="#34c471" />
<l-segmented :value="value" @click="handleClick" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value | 当前选中索引 | number | - |
| size | small/medium/large | string | medium |
| shape | normal/round | string | normal |
| disabled | 禁用 | boolean | false |
| type | button/card/text | string | card |
| bgColor, color, activeColor, sliderColor | 颜色 | string | - |
| fontSize, height, padding | 样式 | string | - |
| immediate | 是否跳过首次动画 | boolean | false |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 切换时 | index: number |
| click | 点击分段时 | index: number |

## 插件标签

- `l-segmented`：组件标签
- `lime-segmented`：演示标签

## 主题定制

--l-segmented-primary-color、--l-segmented-bg-color、--l-segmented-padding-*、--l-segmented-radius、--l-segmented-text-color、--l-segmented-active-*、--l-segmented-*-height、--l-segmented-*-font-size
