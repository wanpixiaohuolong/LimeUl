# LimeSorter 排序按钮

## 介绍

排序按钮组件，用于列表排序。支持 v-model 表示当前方向：1 升序、0 重置、-1 降序；allowReset 双箭头时可重置，descFirst 优先降序；支持插槽自定义箭头。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-sorter label="价格" />
<l-sorter allow-reset>价格</l-sorter>
<l-sorter desc-first>价格</l-sorter>
<l-sorter>
  <text>价格</text>
  <template #arrow="{ value }">...</template>
</l-sorter>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| value / v-model | 选中方向：1 升序，0 重置，-1 降序 | number | - |
| defaultValue | 默认方向 | number | 0 |
| label | 展示文案 | string | - |
| labelStyle | label 样式 | string | - |
| allowReset | 双箭头时是否允许重置 | boolean | false |
| descFirst | 是否优先切换为降序 | boolean | false |
| activeColor | 箭头激活色 | string | - |
| inactiveColor | 箭头未激活色 | string | - |
| arrowSize | 箭头尺寸 | string | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 排序值变化 | value: number |

## Slots 插槽

| 名称 | 说明 | 参数 |
|------|------|------|
| default | 排序项内容 | - |
| arrow | 箭头 | { value: number } |

## 插件标签

- `l-sorter`：组件标签
- `lime-sorter`：演示标签

## 主题定制

--l-sorter-font-size、--l-sorter-color、--l-sorter-arrow-size、--l-sorter-arrow-color、--l-sorter-arrow-active-color（uniappx app 下箭头颜色变量无效）
