# LimeGradientText 渐变文字

## 介绍

原生渲染的渐变文字，支持 linear、radial、conic；deg、colors（数组或位置对象）、gradient 自定义。兼容 uniapp/uniappx。App 端需自定义基座。

**依赖：** `lime-shared`

## 使用

```html
<l-gradient-text text="线性渐变" type="linear" :deg="90" :colors="['#FF0080','#FF8C00','#40E0D0']" />
<l-gradient-text text="45度" type="linear" :deg="45" :colors="['#FF6B6B','#4ECDC4']" />
<l-gradient-text text="径向" type="radial" :colors="['#FF0080','#40E0D0']" />
<l-gradient-text text="锥形" type="conic" :deg="45" :colors="['#FF0000','#FFFF00','#00FF00']" />
<l-gradient-text type="linear" :colors="{0:'#FF0000',50:'#00FF00',100:'#0000FF'}" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| text | 文本内容 | string | - |
| type | linear/radial/conic | string | linear |
| deg | 渐变角度 0–360 | number | 0 |
| colors | 颜色数组或位置对象 {0:'red',100:'blue'} | string[] \| object | [] |
| gradient | 自定义渐变样式覆盖 | string \| object | null |

## 插件标签

- `l-gradient-text`：组件标签
- `lime-gradient-text`：演示标签

## 主题定制

无
