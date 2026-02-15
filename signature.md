# LimeSignature 写字板

## 介绍

手写签名组件，支持横屏、压感模拟(openSmooth)、清空、撤销、重做、保存为图片。用于业务签名等场景。uvue 不支持 openSmooth。

## 使用

```html
<view style="width:750rpx;height:750rpx;">
  <l-signature ref="signatureRef" :penColor="penColor" :penSize="penSize" :openSmooth="openSmooth" disableScroll />
</view>
<button @click="onClick('clear')">清空</button>
<button @click="onClick('undo')">撤销</button>
<button @click="onClick('save')">保存</button>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| penSize | 画笔大小 | number | 2 |
| minLineWidth / maxLineWidth | 线条最小/最大宽度 | number | 2/6 |
| penColor | 画笔颜色 | string | black |
| backgroundColor | 背景色（透明留空） | string | '' |
| openSmooth | 是否模拟压感 | boolean | false |
| landscape | 横屏模式（影响生成图片方向） | boolean | false |
| disableScroll | 禁用滚动 | boolean | true |
| disabled | 禁用写字板 | boolean | false |

## Events 事件

无（通过 ref 调用方法）

## Slots 插槽

无

## Ref 方法

| 名称 | 参数 | 说明 |
|------|------|------|
| clear | - | 清空画板 |
| undo | - | 撤销 |
| redo | - | 重做 |
| canvasToTempFilePath | { success: (res)=>void } | 导出图片，res.tempFilePath、res.isEmpty |

## 插件标签

- `l-signature`：组件标签
- `lime-signature`：演示标签
