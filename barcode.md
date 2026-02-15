# LimeBarcode 条形码

## 介绍

条形码生成组件。支持 text、format(CODE128/EAN13/UPC/CODE39 等)、lineWidth/lineLength、displayValue、font/fontSize/textAlign/textPosition、background/lineColor、margin 及各向 margin、flat、ean128。ref.canvasToTempFilePath 或 useCanvasToTempFilePath + @success。uniappx app 需 lime-barcodegen，部分格式受限。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-barcode text="1234567890" />
<l-barcode text="1234567890" format="CODE128" />
<l-barcode text="1234567890" :line-width="2" :line-length="50" />
<l-barcode text="1234567890" :display-value="false" />
<l-barcode text="1234567890" display-value="自定义文本" />
<l-barcode line-color="#1989fa" background="#f5f5f5" />
<l-barcode ref="ref" text="..." /><button @click="ref.canvasToTempFilePath(...)">生成图片</button>
<l-barcode use-canvas-to-temp-file-path @success="onSuccess" text="..." />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| text | 条形码内容 | string \| number | - |
| format | CODE128/EAN13/UPC/CODE39 等 | string | - |
| lineWidth, lineLength | 线宽/线长 | string \| number | - |
| displayValue | 是否显示下方文本或自定义文本 | string \| boolean | true |
| font, textAlign, textPosition, textMargin, fontSize | 文本样式 | string \| number | - |
| background, lineColor | 背景/线条颜色 | string | - |
| margin, marginTop, marginBottom, marginLeft, marginRight | 边距 | string \| number | - |
| flat, ean128 | 扁平样式/EAN-128 | boolean \| string | - |
| lStyle | 自定义样式 | string | - |
| useCanvasToTempFilePath | 自动导出临时文件 | boolean | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| success | 生成完成 | path: string |

## Ref 方法

canvasToTempFilePath({ success, fail })

## 插件标签

- `l-barcode`：组件标签
- `lime-barcode`：演示标签

## 主题定制

无单独主题变量
