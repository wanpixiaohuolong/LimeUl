# LimePagination 分页

## 介绍

分页组件。v-model 绑定当前页；total、pageSize、pagerCount；hideOnSinglePage、disabled、forceEllipses、simple；showPrevButton/showNextButton、prevText/nextText；bgColor/color/activeBgColor/activeColor 等样式；prev/next/page 插槽、@change。

**依赖：** `lime-style`、`lime-shared`

## 使用

```html
<l-pagination v-model="currentPage" :total="24" :page-size="5" :pager-count="3" />
<l-pagination v-model="currentPage" :total="24" :simple="true" />
<l-pagination v-model="currentPage" :total="204" :page-size="5" force-ellipses />
<l-pagination :show-prev-button="false" :show-next-button="false" />
<l-pagination :disabled="true" />
<l-pagination>
  <template #prev="{ disabled }">←</template>
  <template #page="{ label, active }">{{ label }}</template>
  <template #next="{ disabled }">→</template>
</l-pagination>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model | 当前页码 | number | - |
| total | 总记录数 | number | 0 |
| pageSize | 每页条数 | number | 10 |
| pagerCount | 显示的页码按钮数 | number | 5 |
| hideOnSinglePage | 单页是否隐藏 | boolean | false |
| disabled | 禁用 | boolean | false |
| forceEllipses | 显示省略号 | boolean | false |
| simple | 简单模式 | boolean | false |
| showPrevButton, showNextButton | 显示上一页/下一页 | boolean | true |
| prevText, nextText | 上一页/下一页文字 | string | 上一页/下一页 |
| bgColor, color, activeBgColor, activeColor | 颜色 | string | - |
| fontSize, radius, borderColor | 样式 | string | - |
| itemWidth, itemHeight | 每项宽高 | string | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 切换页 | page: number |

## Slots 插槽

prev（{ disabled }）、next（{ disabled }）、page（{ label, active }）。

## 插件标签

- `l-pagination`：组件标签
- `lime-pagination`：演示标签

## 主题定制

--l-pagination-font-size、--l-pagination-item-width/height、--l-pagination-text-color、--l-pagination-bg-color、--l-pagination-active-*、--l-pagination-disabled-*、--l-pagination-gap、--l-pagination-border-color
