# LimeIcon 图标

## 介绍

图标组件，支持字体图标、Iconify 图标和图片图标。可自定义颜色、大小、前缀等。依赖 `lime-svg` 为收费插件，不需要 SVG 功能可删除。

## 使用

```html
<l-icon name="circle" />
<l-icon name="ri:account-box-fill" color="#1989fa" size="40" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| name | 图标名称、URL 或 Unicode 字符 | string | '' |
| prefix | 图标前缀 | string | l |
| color | 图标颜色 | string | '' |
| size | 图标尺寸 | string/number | 16px |
| inherit | 是否继承颜色 | boolean | true |
| web | 原生 app 是否用 web 渲染 | boolean | false |
| lClass | 自定义类名 | string | '' |
| lStyle | 自定义样式 | string/object/array | '' |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| click | - | 点击事件 |

## Slots 插槽

无

## Ref 方法 / 工具函数

- `registerFontIcon(config)`：注册字体图标库
- `registerIconify(config)`：注册 Iconify 图标库
- `setIconifyApi(url)`：设置默认 Iconify API 地址
- `getIconifyApi()`：获取当前 API 地址
- `parseIconName(name, prefix?)`：解析图标名称
- `useIcon(name, options?)`：核心 Hook，返回图标信息
- `font(iconName, prefix?)`：获取字体图标对应 Unicode

## 插件标签

- `l-icon`：组件标签
- `lime-icon`：演示标签

## 主题定制 CSS 变量

| 变量名 | 默认值 | 描述 |
|--------|--------|------|
| --l-icon-size | 16px | 图标大小 |
| --l-icon-color | - | 图标颜色（仅 icon-font 生效） |
