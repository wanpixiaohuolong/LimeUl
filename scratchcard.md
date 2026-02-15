# LimeScratchcard 刮刮卡

## 介绍

刮刮卡组件，用于刮奖、优惠券等。支持 content 刮开后内容、width/height、coverColor/coverImg 刮层、scratchRadius、backgroundColor、ratio 刮开比例阈值、水印 watermarkText/watermarkColor/watermarkSize、title/titleSize/titleColor、fontSize、default 插槽自定义刮开后内容、@open/@init。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-scratchcard content="恭喜中奖！" />
<l-scratchcard content="恭喜中奖！" :width="200" :height="100" />
<l-scratchcard content="恭喜中奖！" :scratch-radius="15" cover-color="#999999" />
<l-scratchcard watermark-text="活动专用" watermark-color="rgba(0,0,0,0.2)" />
<l-scratchcard><template #default>自定义刮开后内容</template></l-scratchcard>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| content | 刮开后显示的内容 | string | '' |
| height | 高度 | number | 50 |
| width | 宽度 | number | 300 |
| coverColor | 刮层颜色 | string | #d3d3d3 |
| coverImg | 刮层背景图 | string | '' |
| fontSize | 内容字体大小 | number | 20 |
| scratchRadius | 刮开笔触半径 | number | 10 |
| backgroundColor | 背景色 | string | white |
| ratio | 刮开比例阈值(0-1) | number | 0.5 |
| watermarkSize | 水印字体大小 | number | 14 |
| watermarkText | 水印文字 | string | '' |
| watermarkColor | 水印颜色 | string | rgba(0,0,0,0.1) |
| titleSize | 标题字体大小 | number | 24 |
| title | 标题文字 | string | '' |
| titleColor | 标题颜色 | string | rgba(0,0,0,0.8) |

## Events 事件

| 名称 | 说明 |
|------|------|
| open | 刮开时触发 |
| init | 初始化完成时触发 |

## Slots 插槽

default：自定义刮开后的内容。

## 插件标签

- `l-scratchcard`：组件标签

## 主题定制

无单独主题变量
