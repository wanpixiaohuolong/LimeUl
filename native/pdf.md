# LimePdf PDF 预览

## 介绍

UTS 原生 PDF 预览器，支持本地/网络 PDF、密码保护。页面跳转、滑动切换、jumpTo/nextPage/prevPage、动态 render。兼容 web、安卓、iOS、鸿蒙 Next。需自定义基座；安卓需配置 gradle；鸿蒙 Next 需真机+源码。

**依赖：** `lime-shared`

## 使用

```html
<l-pdf ref="pdfRef" url="/static/shareSDK.pdf" @load="load" @fail="fail" @pageChanged="pageChanged" style="height:500px;width:100%" />
<button @click="pdfRef?.jumpTo(3)">跳转指定页</button>
```

```js
// 动态渲染
pdfRef.value?.render('/static/shareSDK.pdf', 0, false, 'password')
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| url | PDF 地址(本地/网络) | string | - |
| page | 当前页索引(从 0 开始) | number | 0 |
| swipeHorizontal | 是否水平滑动切换(仅 uniappx 安卓/ios) | boolean | false |
| password | PDF 密码 | string | - |
| scrollView | 是否内部 scrollView(仅安卓) | boolean | false |
| backTop | 是否显示回到顶部(仅 uniapp) | boolean | false |
| zoomEnable | 是否允许缩放(仅 uniapp) | boolean | true |
| scrollEnable | 是否允许滚动(仅 uniapp) | boolean | true |
| spacing | 页间隔(仅 uniappx 鸿蒙/安卓) | number | - |
| renderType | 渲染方式 svg/canvas(仅 uniapp) | string | canvas |

## Events 事件

load(info)、fail(err)、pageChanged(info)。

## Ref 方法

jumpTo(page)、nextPage()、prevPage()、render(url, page?, swipeHorizontal?, password?)。

## 插件入口

`lime-pdf`：组件 l-pdf
