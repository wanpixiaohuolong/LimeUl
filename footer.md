# LimeFooter 页脚

## 介绍

页脚组件，用于版权与链接。支持 text、links({ name, url?, openType? })、logo({ icon, title, url?, target? })、linkColor/lineColor/textColor/color。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-footer text="Copyright © 2024-2025 LimeUI. All Rights Reserved." />
<l-footer :links="[{ name: '用户协议', url: '/pages/agreement' }, { name: '隐私政策', url: '/pages/privacy' }]" text="Copyright ..." />
<l-footer :logo="{ icon: '/static/logo.png', title: '品牌名称' }" text="Copyright ..." />
<l-footer :logo="{ icon: '...', title: '...', url: '/pages/index' }" :links="[...]" text="..." />
<l-footer link-color="#1989fa" line-color="#dcdee0" text-color="#646566" color="#323233" />
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| links | 导航链接列表 | Object[] | [] |
| logo | Logo 配置 { icon, title, url?, target? } | Object | - |
| text | 版权文本 | string | - |
| linkColor | 链接颜色 | string | - |
| lineColor | 分隔线颜色 | string | - |
| textColor | 版权文本颜色 | string | - |
| color | 文字颜色 | string | - |

## 插件标签

- `l-footer`：组件标签
- `lime-footer`：演示标签

## 主题定制

--l-footer-text-*、--l-footer-link-*、--l-footer-logo-*
