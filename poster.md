# LimePoster 海报生成

## 介绍

海报生成组件，通过 board(JSON) 配置生成含图片、文字、二维码等的海报，支持 ref.render()、ref.toDataURL()、ref.canvasToTempFilePath() 导出。board 结构：style + children；children 元素 type：image、text、view、qrcode。收费组件，免费可看海报画板。

**依赖：** 无（按插件说明）

## 使用

```html
<l-poster :board="posterData" ref="posterRef" @success="onSuccess" @fail="onFail" @progress="onProgress" />
```

```js
const posterData = {
  style: { background: '...', width: '750rpx', paddingBottom: '40rpx' },
  children: [
    { type: 'image', src: '...', style: { width: '84rpx', height: '84rpx', borderRadius: '50%' } },
    { type: 'view', style: {...}, children: [
      { type: 'text', text: '标题', style: { fontSize: '32rpx', color: '#fff' } }
    ]},
    { type: 'qrcode', text: 'https://...', style: { width: '128rpx', height: '128rpx' } }
  ]
}
// 导出
const url = await posterRef.value.toDataURL()
posterRef.value.canvasToTempFilePath({ success(res) { console.log(res.tempFilePath) } })
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| board | 海报画板数据(style+children) | UTSJSONObject | - |
| pixelRatio | 像素比 | number | 设备像素比 |
| hidden | 是否隐藏不渲染 | boolean | false |
| generateTempFile | 是否生成临时文件路径 | boolean | false |
| useCORS | 是否 CORS(仅 WEB) | boolean | false |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| success | 生成临时文件成功 | - |
| fail | 生成失败 | error |
| progress | 生成进度 | progressValue |

## Ref 方法

render(board)、toDataURL()、canvasToTempFilePath({ success, fail })

## board 结构简述

- style：整体样式(background、width、padding 等)
- children：元素数组；元素 type：image(src)、text(text)、view(children)、qrcode(text)；style 支持 width、height、margin、padding、fontSize、color、borderRadius 等(驼峰，单位 rpx/px)

## 插件标签

- `l-poster`：组件标签

## 主题定制

无
