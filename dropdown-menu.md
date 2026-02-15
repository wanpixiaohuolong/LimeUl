# LimeDropdownMenu 下拉菜单

## 介绍

顶部/底部筛选菜单，多个 l-dropdown-item 并列。支持 options 选项、自定义插槽内容、自定义标题(label/插槽)、activeColor、横向滚动(spaceEvenly)、向上展开(direction="up")。**付费组件。**

**依赖：** `lime-popup`、`lime-icon`、`lime-svg`、`lime-shared`、`lime-style`

## 使用

```html
<l-dropdown-menu>
  <l-dropdown-item v-model="value1" :options="option1" />
  <l-dropdown-item v-model="value2" :options="option2" />
</l-dropdown-menu>
<l-dropdown-menu active-color="#ee0a24" direction="up">
  <l-dropdown-item v-model="value2" label="筛选" ref="itemRef">
    <view class="cell">...</view>
    <button @click="itemRef?.toggle?.(null)">确认</button>
  </l-dropdown-item>
</l-dropdown-menu>
```

## DropdownMenu Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| activeColor | 选中态颜色 | string | - |
| direction | up / down | string | down |
| zIndex | 层级 | number | 999 |
| duration | 动画时长(ms)，0 禁用 | number | - |
| overlay | 是否显示遮罩 | boolean | true |
| closeOnClickOverlay | 点击遮罩关闭 | boolean | true |
| closeOnClickOutside | 点击外部关闭 | boolean | true |
| spaceEvenly | 是否均分；false 可横向滚动 | boolean | true |
| bgColor / color | 背景色/文本色 | string | - |

## DropdownItem Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| v-model | 当前选中 value | number \| string | - |
| options | 选项数组 { label, value, disabled? } | array | [] |
| keys | value/label 字段别名 | object | - |
| disabled | 是否禁用 | boolean | false |
| defaultValue | 非受控默认值 | number \| string | - |

## DropdownItem Events

| 名称 | 说明 | 回调 |
|------|------|------|
| change | 选项导致值变化 | value |
| open / close | 打开/关闭 | - |
| opened / closed | 动画结束后的打开/关闭 | - |

## DropdownItem Slots

| 名称 | 说明 |
|------|------|
| default | 菜单内容（自定义时需手动 toggle 关闭） |
| label | 自定义标题，参数 { visible } |

## Ref 方法

- **DropdownMenu**：close() 关闭所有菜单
- **DropdownItem**：toggle(show?: boolean \| null) 切换显示，true 显示、false 隐藏、null 取反（uniappx 需传 null）

## 插件标签

- `l-dropdown-menu`、`l-dropdown-item`：组件标签
- `lime-dropdown-menu`：演示标签

## 主题定制

--l-dropdown-menu-height、--l-dropdown-menu-bg-color、--l-dropdown-menu-color、--l-dropdown-menu-active-color、--l-dropdown-item-* 等，详见官方文档。
