# LimeCard 卡片

## 介绍

卡片组件，用于内容区块展示。支持标题、副标题、图标、封面图、操作按钮等，适用于图文、产品、新闻等场景。

**依赖：** `lime-shared`、`lime-style`

---

## 手动修改说明（本项目对 lime-card 源码的修改）

> 以下为在 **uni_modules/lime-card** 插件源码上的手动修改，便于统一关闭 body 留白与横向/竖向排版，无需在各页面写 `.l-card__body` 覆盖样式。若从插件市场重新安装 lime-card，需重新应用以下修改或使用本仓库备份的组件。

### 修改内容概览

| 修改项 | 说明 |
|--------|------|
| **新增 4 个 Props** | `bodyInset`、`bodyDirection`、`bodyJustify`、`bodyGap` |
| **body 修饰类** | `l-card__body--no-inset`、`--row`、`--column`、`--justify-*` |
| **涉及文件** | `type.ts`、`props.ts`、`l-card.uvue`、`l-card.vue`、`index.scss`、`readme.md` |

### 具体改动

1. **type.ts / props.ts**  
   - 新增 `bodyInset?: boolean`，默认 `false`（默认关闭 body 留白）。为 `true` 时 body 有默认 padding、margin。  
   - 新增 `bodyDirection?: 'row' | 'column'`，默认 `'column'`。  
   - 新增 `bodyJustify?: 'start' | 'end' | 'center' | 'space-around' | 'space-between'`，默认 `'start'`（body 为 row 时生效）。  
   - 新增 `bodyGap?: string`，body 为 row 时的子项间距（如 `'28rpx'`）。

2. **l-card.uvue / l-card.vue 模板**  
   - `l-card__body` 上根据 props 绑定 class：  
     `l-card__body--no-inset`（`!bodyInset`）、  
     `l-card__body--row` / `l-card__body--column`（`bodyDirection`）、  
     `l-card__body--justify-start` 等（`bodyJustify`）。  
   - 当 `bodyDirection === 'row'` 且 `bodyGap` 有值时，body 的 `:style` 设置 `gap: bodyGap`。

3. **index.scss**  
   - `&__body--no-inset`：`padding: 0 !important; margin: 0 !important;`  
   - `&__body--row`：`display: flex; flex-direction: row; align-items: center; min-width: 0;`  
   - `&__body--column`：`display: flex; flex-direction: column; min-width: 0;`  
   - `&__body--justify-start` 等：对应 `justify-content`。

4. **readme.md**  
   - 在 Props 表格中补充上述 4 个属性的说明与默认值。

---

## 使用

```html
<!-- 基础 -->
<l-card title="卡片标题" note="副标题" extra="更多" more>
  <text>卡片内容</text>
</l-card>

<!-- 带封面、操作 -->
<l-card title="标题" cover="https://..." coverMode="aspectFill" :actions="actions" />

<!-- 关闭 body 留白 + 横向排版（需使用上述源码修改后的组件） -->
<l-card :inset="false" :bodyInset="false" bodyDirection="row" bodyJustify="space-around" bodyGap="28rpx">
  <view>左</view>
  <view>中</view>
  <view>右</view>
</l-card>

<!-- 仅关闭 body 留白，竖向排版 -->
<l-card :inset="false" :bodyInset="false" bodyDirection="column">
  <text>内容</text>
</l-card>
```

---

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| title | 卡片标题 | string | - |
| note | 同行说明文字 | string | - |
| extra | 右侧额外文字 | string | - |
| icon | 左侧图标名称 | string | - |
| image | 左侧图片地址 | string | - |
| cover | 封面图地址 | string | - |
| more | 是否显示更多图标 | boolean | false |
| inset | 是否内嵌样式 | boolean | true |
| **bodyInset** | **是否使用 body 内边距/外边距（true 时 body 有默认 padding、margin）** | **boolean** | **false** |
| **bodyDirection** | **body 排版方向：`row` 横向、`column` 竖向** | **string** | **'column'** |
| **bodyJustify** | **body 为 row 时的对齐：start/end/center/space-around/space-between** | **string** | **'start'** |
| **bodyGap** | **body 为 row 时的子项间距（如 28rpx）** | **string** | - |
| actions | 操作按钮列表 | Array | - |
| actionsAlign | 操作对齐 left/right/space-between | string | right |
| iconColor / rightIcon / rightIconColor | 图标相关 | string | - |
| iconSize / rightIconSize | 图标尺寸 | string | - |
| lStyle / imageStyle / coverStyle | 自定义样式 | string \| object | - |
| coverMode | 封面图裁剪模式 | string | widthFix |
| bgColor | 卡片背景色 | string | - |
| headerBordered | 是否头部边框 | boolean | true |
| footerBordered | 是否底部边框 | boolean | true |
| lClass / lClassLeftIcon / lClassRightIcon | 自定义类名 | string | - |

**bodyDirection 可选值：** `row`（横向）、`column`（竖向）  
**bodyJustify 可选值：** `start`、`end`、`center`、`space-around`、`space-between`  

**coverMode 可选值：** scaleToFill、aspectFit、aspectFill、widthFix、heightFix、top、bottom、center、left、right 等

---

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| action | index: number | 点击操作按钮 |
| more | event: UniEvent | 右侧更多点击 |
| getuserinfo / contact / getphonenumber / error / opensetting / launchapp / chooseavatar / agreeprivacyauthorization | event: UniEvent | 开放能力回调 |

---

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 卡片内容 |
| cover | 自定义封面 |
| title | 自定义标题区域 |
| icon | 自定义图标 |
| header-extra | 自定义头部右侧 |
| footer | 自定义底部 |

---

## Action 按钮配置

与 lime-button 一致，含 content、type、block、disabled、icon、loading、ghost、shape、size、variant、color、textColor、fontSize 等。

---

## 插件标签

- `l-card`：组件标签
- `lime-card`：演示标签

---

## 主题定制

提供大量 CSS 变量，如 `--l-card-header-line-height`、`--l-card-header-padding-y`、`--l-card-header-padding-x`、`--l-card-bg-color`、`--l-card-title-color`、`--l-card-border-radius` 等，详见组件 readme。
