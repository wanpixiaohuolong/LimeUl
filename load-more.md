# LimeLoadMore 加载更多

## 介绍

列表底部“加载更多”组件，支持 remaining/loading/finished/error 四种状态，可自定义文案与样式。remaining 点击触发 load-more，error 点击触发 reload。

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-load-more status="remaining" @load-more="load" />
<l-load-more status="loading" loading-text="努力加载中" />
<l-load-more status="finished" finished-text="已经完成" />
<l-load-more status="error" @reload="reload" />
<l-load-more :status="status" line line-color="#dcdee0" height="60" content-color="#1989fa" />
```

## 状态说明

| 状态 | 交互 | 场景 |
|------|------|------|
| remaining | 点击触发 load-more | 未满一屏需手动加载 |
| loading | 禁用交互 | 请求中 |
| finished | 禁用交互 | 全部加载完毕 |
| error | 点击触发 reload | 失败需重试 |

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| status | 状态 | string | remaining |
| remainingText | remaining 文案 | string | - |
| loadingText | loading 文案 | string | - |
| finishedText | finished 文案 | string | - |
| errorText | error 文案 | string | - |
| loadingColor | 加载图标颜色 | string | - |
| loadingSize | 加载图标大小 | string | - |
| color | 文本颜色 | string | - |
| fontSize | 字体大小 | string | - |
| line | 是否显示分割线 | boolean | - |
| lineColor | 分割线颜色 | string | - |
| height | 高度 | string | - |

## Events 事件

| 名称 | 说明 |
|------|------|
| load-more | status 为 remaining 时点击触发 |
| reload | status 为 error 时点击触发 |

## Slots 插槽

| 名称 | 说明 |
|------|------|
| remaining | 还有更多可加载 |
| loading | 正在加载中 |
| error | 加载失败 |
| finished | 全部加载完成 |

## 插件标签

- `l-load-more`：组件标签
- `lime-load-more`：演示标签

## 主题定制

--l-load-more-height、--l-load-more-text-color、--l-load-more-font-size、--l-load-more-color、--l-load-more-icon-size、--l-load-more-gap。uniappx app 下 --l-load-more-color 无效。
