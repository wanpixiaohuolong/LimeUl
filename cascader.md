# LimeCascader 级联选择

## 介绍

多层级数据选择组件，主要为树形结构。支持自定义字段名、每级次标题、激活色、中国省市区数据、uniCloud 数据源。兼容 uniapp/uniappx。

**依赖：** `lime-popup`、`lime-style`、`lime-shared`、`lime-tabs`、`lime-icon`、`lime-svg`

## 使用

```html
<view @click="visible = true">
  <text>{{ fieldValue || '请选择地址' }}</text>
</view>
<l-cascader
  v-model:visible="visible"
  v-model="cascaderValue"
  :options="options"
  title="请选择所在地区"
  @change="onChange"
/>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model:visible | 是否显示级联选择器 | boolean | false |
| v-model | 选中值（最后一级 value） | string | - |
| options | 可选项数据源，children 为子选项 | array | - |
| subTitles | 每级展示的次标题 | string[] | - |
| placeholder | 未选中时的提示文案 | string | 选择选项 |
| keys | value/label/children 在 options 中的字段别名 | {label,value,children} | {} |
| title | 标题 | string | - |
| closeable | 是否显示关闭按钮 | boolean | - |
| bgColor | 背景色 | string | - |
| activeColor | 激活色 | string | - |
| iconSize / color / fontSize | 图标与文本样式 | string | - |
| confirmBtn | 确认按钮：null 不显示；string 按钮文案；Object 透传 Button 属性 | string \| Object | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| pick | (level, index, value, selectedIndexes) | 选择某一级时触发 |
| change | (value: string, options: UTSJSONObject[]) | 全部选完时触发 |
| close | - | 关闭时触发 |

## Slots 插槽

无

## 数据与扩展

- **options 结构：** 每项含 `label`、`value`，子级为 `children` 数组；可用 `keys` 映射为其他字段名（如 name/code/items）。
- **中国省市区：** `import { useCascaderAreaData } from '@/uni_modules/lime-shared/areaData'`，`const options = useCascaderAreaData()`。
- **uniCloud：** 设置 `uniCloud` 可加载 `opendb-city-china` 表数据。

## 插件标签

- `l-cascader`：组件标签
- `lime-cascader`：演示标签

## 主题定制 CSS 变量

--l-cascader-title-color、--l-cascader-icon-color、--l-cascader-bg-color、--l-cascader-height、--l-cascader-cell-height、--l-cascader-cell-title-color、--l-cascader-disabled-color、--l-cascader-close-icon-color 等，详见组件文档。
