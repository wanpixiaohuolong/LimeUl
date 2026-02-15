# LimeCountTo 数字滚动

## 介绍

数字滚动动画组件。支持 from/to、precision、showSeparator(千位/万分位 separator)、duration、active 激活动画、ref.play()、@finish、formatted 插槽(value.integer/decimal)。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-count-to :to="1000" />
<l-count-to :from="0" :to="1000" />
<l-count-to :to="1000.56789" :precision="2" />
<l-count-to :to="1000000" show-separator />
<l-count-to :to="1000000" show-separator separator="group4" />
<l-count-to :to="1000" :duration="3000" />
<l-count-to :active="false" ref="ref" /><button @click="ref.play()">播放</button>
<l-count-to :to="699700.699" :precision="3" @finish="handleFinish">
  <template #formatted="{ value }">￥{{ value.integer }}.{{ value.decimal }}</template>
</l-count-to>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| to | 目标值 | number | 0 |
| from | 起始值 | number | 0 |
| precision | 小数位数 | number | 0 |
| showSeparator | 是否千位分隔 | boolean | false |
| separator | group3/group4 | string | group3 |
| locale | 国际化 | string | - |
| active | 是否激活动画 | boolean | true |
| duration | 动画时长(ms) | number | 2000 |
| timingFunction | 缓动函数 | function | null |
| fps | 帧率，0 默认 | number | 0 |

## Events 事件

| 名称 | 说明 |
|------|------|
| finish | 动画结束 |

## Slots 插槽

| 名称 | 说明 | 参数 |
|------|------|------|
| formatted | 自定义展示 | { value: { integer, decimal, decimalSeparator } } |

## Ref 方法

play()

## 插件标签

- `l-count-to`：组件标签
- `lime-count-to`：演示标签

## 主题定制

无单独主题变量说明（使用通用字体/颜色）
