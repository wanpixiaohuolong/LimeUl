# LimeSteps 步骤条

## 介绍

步骤条，由 l-steps + l-step 组成。current 表示当前步骤索引，支持横向/竖向(layout)、图标、dot 简略模式、状态(wait/process/finish/error)、activeColor/finishBgColor、ref 等。

**依赖：** `lime-shared`、`lime-style`（lime-svg 可选）

## 使用

```html
<l-steps :current="current" @change="change">
  <l-step title="买家下单" content="辅助信息" />
  <l-step title="商家接单" content="辅助信息" />
  <l-step title="交易完成" content="辅助信息" />
</l-steps>
<l-steps :current="current" type="dot">...</l-steps>
<l-steps :current="current" layout="vertical">...</l-steps>
<l-step title="商家接单" status="error" />
<l-step><template #extra>自定义额外内容</template></l-step>
```

## Steps Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| current / value / modelValue | 当前步骤索引 | number | - |
| defaultCurrent | 默认当前步骤 | number | - |
| status | 当前步骤状态 | string | process |
| layout | horizontal / vertical | string | horizontal |
| readonly | 是否只读 | boolean | false |
| sequence | 步骤顺序 | string | positive |
| type | default / dot | string | default |
| activeColor, finishBgColor, waitColor, waitBgColor | 颜色 | string | - |

## Step Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| title | 标题 | string | - |
| content | 描述 | string | - |
| titleRight | 标题右侧信息 | string | - |
| icon | 图标名 | string | - |
| status | wait/process/finish/error | string | wait |

## Steps Events

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 当前步骤变化 | index: number |

## Step Slots

icon、title、content、extra。

## 插件标签

- `l-steps`、`l-step`：组件标签
- `lime-steps`：演示标签

## 主题定制

--l-step-dot-size、--l-step-circle-*、--l-step-description-color、--l-step-wait-*、--l-step-process-*、--l-step-finish-*、--l-step-error-*、--l-step-line-*
