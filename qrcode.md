# LimeQrcode 二维码

## 介绍

二维码生成组件。支持 value、size、color/bgColor、icon/iconSize、marginSize、bordered、errorLevel(L/M/Q/H)、useCanvasToTempFilePath 自动导出、use2d。ref.canvasToTempFilePath() 生成图片；@complete/@error。uniappx app 需依赖 lime-qrcodegen。

**依赖：** `lime-shared`

## 使用

```html
<l-qrcode value="http://lime.qcoon.cn" />
<l-qrcode value="https://..." size="300rpx" icon="/static/logo.png" icon-size="70rpx" />
<l-qrcode value="https://..." color="rgb(82,196,26)" bg-color="..." />
<l-qrcode value="..." error-level="H" />
<l-qrcode ref="ref" value="..." /><button @click="ref.canvasToTempFilePath({ success, fail })">生成图片</button>
<l-qrcode use-canvas-to-temp-file-path @complete="onComplete" value="..." />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| value | 二维码内容 | string | - |
| size | 尺寸 | number \| string | 160 |
| color | 前景色 | string | #000 |
| bgColor | 背景色 | string | transparent |
| icon | 中心图标 | string | - |
| iconSize | 图标大小 | number \| string | 40 |
| marginSize | 外边距 | number | - |
| bordered | 显示边框 | boolean | true |
| errorLevel | L/M/Q/H | string | M |
| useCanvasToTempFilePath | 自动导出临时文件 | boolean | false |
| use2d | 使用 2D Canvas | boolean | true |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| complete | 生成完成 | path: string（useCanvasToTempFilePath 时） |
| error | 生成失败 | error: Error |

## Ref 方法

canvasToTempFilePath({ success, fail })

## 插件标签

- `l-qrcode`：组件标签
- `lime-qrcode`：演示标签

## 主题定制

无单独主题变量
