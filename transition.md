# LimeTransition 过渡动画

## 介绍

过渡动画组件，使元素从一种样式逐渐变为另一种样式。支持多种动画类型、自定义时长，兼容 uni-app 和 uni-app x。

**依赖：** `lime-shared`

## 使用

```html
<l-transition :visible="show" :appear="true" name="fade-up">
  <view class="box">内容</view>
</l-transition>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| name | 动画类型 | string | fade |
| visible | 是否展示 | boolean | true |
| appear | 首次出现是否执行动画 | boolean | false |
| destoryOnClose | 隐藏时是否销毁内容 | boolean | false |
| duration | 动画时长(ms) | number | 300 |
| zIndex | 层级 | number | 11000 |
| l-style | 自定义样式 | string | - |

**name 可选值：** fade、fade-up、fade-down、fade-left、fade-right、slide-up、slide-down、slide-left、slide-right

## Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| before-enter | - | 进入前 |
| enter | - | 进入中 |
| after-enter | - | 进入后 |
| before-leave | - | 离开前 |
| leave | - | 离开中 |
| after-leave | - | 离开后 |

## Slots 插槽

无（包裹需动画的内容即可）

## 插件标签

- `l-transition`：组件标签
- `lime-transition`：演示标签

## 外部样式类（小程序需全局设置）

enter-class、enter-active-class、enter-to-class、leave-class、leave-active-class、leave-to-class、l-class
