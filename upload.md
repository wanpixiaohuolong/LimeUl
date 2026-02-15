# LimeUpload 文件上传

## 介绍

文件上传组件，支持图片/视频、uniCloud 与自定义服务器、多选、预览、上传状态与进度、自定义上传区域。兼容 uniapp/uniappx。`mediaType="all"` 需 lime-choose-file 原生插件。

**依赖：** `lime-style`、`lime-shared`、`lime-icon`、`lime-svg`

## 使用

```html
<l-upload @add="handleAdd" />
<l-upload v-model="files" :max="5" action="https://example.com/upload" :autoUpload="true" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model | 双向绑定文件列表 | UploadFile[] | - |
| defaultFiles | 默认已传文件列表 | UploadFile[] | - |
| disabled / readonly | 禁用/只读 | boolean | false |
| multiple | 是否多选 | boolean | true |
| disablePreview | 是否禁用预览 | boolean | false |
| autoUpload | 是否自动上传 | boolean | false |
| action | 上传地址，'uniCloud' 表示云存储 | string | - |
| headers | 额外请求头/表单数据 | object | - |
| mediaType | 类型 'image'/'video'/'media' | string | image |
| max | 最大数量，0 不限制 | number | 100 |
| maxDuration | 视频最长时长(秒) | number | 10 |
| sizeType | ['original','compressed'] | string[] | - |
| sourceType | ['album','camera'] | string[] | - |
| sizeLimit | 文件大小限制(KB) | number | - |
| column | 列数 | string/number | - |
| gutter | 格子间隔 | string | 8px |
| gridWidth / gridHeight | 格子宽高 | string | 80px |
| gridBgColor / gridBorderRadius | 格子样式 | string | - |
| addBgColor | 上传格背景色 | string | - |
| uploadIcon / uploadIconSize | 上传图标 | string/number | - |
| loadingText / reloadText / failedText | 状态文案 | string | - |
| imageFit | 预览图裁剪模式 | string | - |

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| add | files: LimeUploadFile[] | 选择文件后触发 |
| remove | { index, file } | 删除文件时触发 |
| success | results: UploadResult[] | 全部上传成功 |
| fail | error: Error | 任意文件上传失败 |
| click | { file } | 点击文件区域 |

## Slots 插槽

默认插槽：完全自定义上传区域内容。

## Ref 方法

| 名称 | 参数 | 说明 |
|------|------|------|
| remove | index: number | 删除指定索引文件 |

## LimeUploadFile 类型

name, url, type, status('loading'|'reload'|'failed'|'done'), percent, path, size。

## 插件标签

- `l-upload`：组件标签
- `lime-upload`：演示标签

## 主题定制

--l-upload-radius、--l-upload-width/height、--l-upload-bg-color、--l-upload-delete-*、--l-upload-add-* 等。
