# LimeSwitch 开关

## 介绍

开关组件，用于开启/关闭某一功能。支持禁用、加载态、圆形/方形、占位文案、自定义尺寸与颜色、异步控制。兼容 uniapp/uniappx。

**依赖：** `lime-style`、`lime-loading`、`lime-shared`

## 使用

```html
<l-switch v-model="checked" />
<l-switch v-model="checked" :placeholder="['开', '关']" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model / value / defaultValue | 开关选中状态 | boolean | false |
| disabled / readonly | 禁用/只读 | boolean | false |
| loading | 加载中 | boolean | false |
| round | 是否圆形（false 为方形） | boolean | true |
| rubberBand | 按钮是否有橡皮筋效果 | boolean | true |
| placeholder | 占位内容 [开启时, 关闭时] | string[] | [] |
| fontSize | 字体大小 | string | - |
| width / height | 开关最小宽度/高度 | string | - |
| dotSize / dotPressedSize | 按钮尺寸/按下时尺寸 | string | - |
| checkedColor | 打开时背景色 | string | - |
| uncheckedColor | 关闭时背景色 | string | - |
| disabledColor / checkedDisabledColor | 禁用态背景色 | string | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | currentValue: boolean | 开关状态切换时触发 |

## Slots 插槽

| 名称 | 说明 | 参数 |
|------|------|------|
| icon | 按钮上图标/文案 | { checked } |

## 插件标签

- `l-switch`：组件标签
- `lime-switch`：演示标签

## 主题定制 CSS 变量

--l-switch-checked-color、--l-switch-unchecked-color、--l-switch-width/height、--l-switch-dot-size、--l-switch-*-radius、--l-switch-dot-bg-color、--l-switch-font-size、--l-switch-text-color 等。
