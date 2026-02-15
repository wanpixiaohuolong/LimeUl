# LimeAmount 金额组件

## 介绍

金额展示与格式化。支持 symbol、precision、showSymbol/showDecimal、showSeparator、separatorDigits、reverse 符号在后、transition 数字动画、capital 中文大写、插槽 integer/decimal/symbol。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-amount value="1234.56" />
<l-amount value="1234.56" symbol="$" />
<l-amount value="1234.56" :show-symbol="false" />
<l-amount value="1234.56789" :precision="3" />
<l-amount value="1234.56" :show-decimal="false" />
<l-amount value="1234567.89" show-separator />
<l-amount value="1234.56" reverse />
<l-amount value="1234.56" transition :duration="2000" />
<l-amount value="1234.56" capital />
<l-amount value="1234.56" font-size="24px" color="#ff5500" />
<l-amount :value="v"><template #default="{ integer, decimal }">{{ integer }}.{{ decimal }}</template></l-amount>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| value | 金额 | number \| string | - |
| symbol | 货币符号 | string | ￥ |
| precision | 小数位数 | number | 2 |
| reverse | 符号在数字后 | boolean | false |
| transition | 数字变化动画 | boolean | false |
| duration | 动画时长(ms) | number | 1000 |
| separatorDigits | 分隔位数(4 为万) | number | 4 |
| separator | 分隔符 | string | , |
| showSymbol | 显示货币符号 | boolean | true |
| showDecimal | 显示小数 | boolean | true |
| showSeparator | 显示分隔符 | boolean | false |
| capital | 中文大写 | boolean | false |
| roundUp | 四舍五入 | boolean | true |
| fontSizeRatio, fontSize, color, lStyle | 样式 | number \| string | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 数值变化 | value: number \| string |

## Slots 插槽

symbol、integer、decimal（或 default 传 { integer, decimal }）。

## 插件标签

- `l-amount`：组件标签
- `lime-amount`：演示标签

## 主题定制

--l-amount-color、--l-amount-font-size、--l-amount-font-weight、--l-amount-font-size-ratio
