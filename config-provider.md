# LimeConfigProvider 全局配置组件

## 介绍

统一管理 LimeUI 组件库的主题样式和变量，支持明暗主题切换、自定义主题变量。作为基础设施为所有组件提供统一主题配置。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-config-provider :theme="currentTheme" :themeVars="themeVars">
  <view><!-- 内部所有 LimeUI 组件使用该主题 --></view>
</l-config-provider>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| theme | 主题风格，'dark' 开启深色模式 | 'light' \| 'dark' | 'light' |
| themeVars | 自定义主题变量对象，属性名用驼峰命名 | object | {} |
| lClass | 根节点 class | string | - |
| lStyle | 根节点样式 | string \| object | - |

## Events 事件

无

## Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 需要应用主题配置的内容 |

## 插件标签

- `l-config-provider`：组件标签
- `lime-config-provider`：演示标签

## 暗黑模式（深色模式）

### 启用方式

设置 `theme="dark"` 即可开启深色主题，内部 LimeUI 组件会使用暗色样式。

```html
<l-config-provider theme="dark">
  <view class="page">
    <l-button>暗色按钮</l-button>
    <l-input placeholder="暗色输入框"></l-input>
    <l-card title="暗色卡片"><text>暗色模式下的内容</text></l-card>
  </view>
</l-config-provider>
```

### 重要说明

**`l-config-provider` 只影响 LimeUI 组件库的样式**，不会自动改变你的自定义组件或页面的文字颜色、背景颜色。若希望整页（含自定义内容）跟随深色模式，需要自行在样式中使用与深色匹配的变量，并在深色主题下覆盖这些变量。

### 页面与深色模式匹配的样式写法

官方建议：用变量 + `.l-theme-dark` 覆盖，使页面背景、文字、卡片等与深色主题一致。

```scss
// 定义变量（浅色默认值）
$page-bg-color: var(--doc-page-bg-color, #f5f5f5);

// 深色主题下覆盖变量（ConfigProvider 为 dark 时根节点会带 .l-theme-dark）
.l-theme-dark {
  --doc-card-bg-color: #242424;
  --doc-page-bg-color: #181818;
  --doc-title-color: rgba(255, 255, 255, 0.9);
  --doc-summary-color: rgba(255, 255, 255, 0.6);
  --doc-text-color: rgba(255, 255, 255, 0.8);
}

// 页面使用变量，并加过渡
.page {
  background-color: $page-bg-color;
  color: var(--doc-text-color, #333);
  transition: background-color 200ms, color 200ms;
}
```

### 动态切换主题

用响应式数据绑定 `theme` 和 `themeVars`，在切换时同时改 `themeVars`，使自定义变量与当前主题一致。

```html
<l-config-provider :theme="currentTheme" :themeVars="themeVars">
  <view class="page">
    <l-button type="primary" @click="toggleTheme">
      {{ currentTheme === 'light' ? '切换到深色模式' : '切换到浅色模式' }}
    </l-button>
    <l-card title="动态主题演示"><text>点击按钮切换主题</text></l-card>
  </view>
</l-config-provider>
```

```js
const currentTheme = ref('light')
const themeVars = ref({})

const toggleTheme = () => {
  currentTheme.value = currentTheme.value === 'light' ? 'dark' : 'light'
  if (currentTheme.value === 'dark') {
    themeVars.value = {
      primaryColor: '#177ddc',
      textColor1: 'rgba(255, 255, 255, 0.85)',
      cardBgColor: '#1f1f1f',
    }
  } else {
    themeVars.value = {
      primaryColor: '#1677ff',
      textColor1: 'rgba(0, 0, 0, 0.88)',
      cardBgColor: '#ffffff',
    }
  }
}
```

---

## 主题定制说明

- 在 `uni.scss` 可修改固定色值：`$primary-color`、`$error-color`、`$warning-color`、`$info-color`、`$success-color`。
- 页面根节点可覆盖 CSS 变量，如 `page { --l-card-bg-color: #f5f7fa; }`。
- `themeVars` 驼峰名会自动转为连字符 CSS 变量（如 `cardBgColor` → `--l-card-bg-color`）。
- **注意：** uni-app x (app 端) 中 CSS 变量支持尚不完全，部分变量可能不生效。
