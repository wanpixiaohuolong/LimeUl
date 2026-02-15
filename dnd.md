# LimeDnd 拖拽排序

## 介绍

拖拽排序组件，由 l-dnd、l-dnd-item、l-dnd-handle 组成。支持 v-model:list、单列/多列(column)、禁用项(disabled)、useHandle 仅手柄拖拽、longpress、autoScroll 边缘滚动。**付费组件，需源码运行。**

**依赖：** 见插件说明

## 使用

```html
<l-dnd v-model:list="list" @change="onChange">
  <l-dnd-item v-for="(item, i) in list" :key="item.id" :index="i">
    <view class="item">{{ item.text }}</view>
  </l-dnd-item>
</l-dnd>
<l-dnd v-model:list="gridList" :item-height="120" :column="3" :gap="5">
  <l-dnd-item v-for="(item, i) in gridList" :key="item.id" :index="i">...</l-dnd-item>
</l-dnd>
<l-dnd v-model:list="list" use-handle>
  <l-dnd-item v-for="(item, i) in list" :key="item.id" :index="i">
    <text>{{ item.text }}</text>
    <l-dnd-handle><l-icon name="view-list" /></l-dnd-handle>
  </l-dnd-item>
</l-dnd>
```

## Dnd Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| list | 列表数据（v-model:list 双向） | object[] | [] |
| itemHeight | 项高度 | number | 50 |
| column | 列数 | number | 1 |
| gap | 间距 | number | 0 |
| scrollDiff | 滚动差值 | number | 1 |
| useHandle | 仅通过手柄拖拽 | boolean | false |
| longpress | 仅长按触发拖拽 | boolean | false |
| autoScroll | 边缘自动滚动 | boolean | false |
| container | 获取容器 DOMRect 函数 | () => Promise\<DOMRect\> | - |
| lClass / lStyle | 类名/样式 | string \| object | - |

## Dnd Events

| 名称 | 说明 | 回调 |
|------|------|------|
| update:list | 列表更新 | list |
| drag-start | 开始拖拽 | { itemIndex } |
| drag-move | 拖拽移动 | { itemIndex, insertIndex, deltaX, deltaY } |
| edge-scroll | 边缘滚动 | { deltaY } |
| drop | 放下 | { itemIndex, insertIndex } |

## DndItem Props

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| index | 索引（必填） | number | - |
| disabled | 禁用拖拽 | boolean | false |
| lClass / lStyle | 类名/样式 | - | - |

## DndItem Slots

| 名称 | 说明 | 参数 |
|------|------|------|
| default | 项内容 | { active, passive } |

## DndHandle

无 Props，default 插槽为手柄内容。

## 插件标签

- `l-dnd`、`l-dnd-item`、`l-dnd-handle`：组件标签
- `lime-dnd`：演示标签

## 主题定制

--l-dnd-duration、--l-dnd-dragging-shadow（uniappx app 暂时无效）
