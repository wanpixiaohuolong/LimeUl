# LimeColorPicker 颜色选择器

## 介绍

颜色选择器，支持 HEX、RGB、HSB 格式，预设颜色(presets)，受控模式。可用于主题定制、样式设计。常与 Popup 搭配使用。**付费组件。**

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-color-picker v-model="color" />
<l-color-picker :presets="presets" @change="change" />
<l-popup v-model="showPicker" position="bottom">
  <l-color-picker v-model="color" :presets="presets" @change="change" @formatChange="formatChange" />
</l-popup>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| value / v-model | 颜色值(HEX/RGB/HSB) | string | - |
| defaultValue | 默认颜色 | string | - |
| presets | 预设分组 { label, colors: string[] }[] | array | - |
| disabled | 是否禁用 | boolean | false |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| change | value: { hex, rgb, hsb } | 颜色变化时触发 |
| formatChange | format: 'hex'\|'rgb'\|'hsb' | 格式切换时触发 |

## Slots 插槽

无

## 插件标签

- `l-color-picker`：组件标签
- `lime-color-picker`：演示标签

## 主题定制

--l-color-picker-palette-height、--l-color-picker-handle-*、--l-color-picker-input-height、--l-color-picker-preset-*、--l-color-picker-slider-*、--l-color-picker-color/label-color/divider-color 等，详见组件文档。
