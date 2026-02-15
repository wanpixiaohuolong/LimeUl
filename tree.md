# LimeTree 树形组件

## 介绍

树形结构展示与选择。支持 data、keyField/labelField/childrenField、defaultExpandedKeys/expandedKeys、defaultCheckedKeys/checkedKeys、checkable、cascade、checkStrategy(all/parent/child)、expandOnClick、checkOnClick、pattern 搜索、showIrrelevantNodes、loadNode 异步加载、indentWidth、插槽 switcher/content。**付费，仅支持源码。**

**依赖：** `lime-shared`、`lime-style`、`lime-checkbox`、`lime-loading`

## 使用

```html
<l-tree :data="data" :default-expanded-keys="expandedKeys" expand-on-click checkable />
<l-tree :data="data" key-field="id" label-field="name" children-field="items" />
<l-tree :data="data" cascade :default-checked-keys="checkedKeys" @checked="updateChecked" checkable />
<l-tree :data="data" :pattern="pattern" :show-irrelevant-nodes="showIrrelevant" />
<l-tree :data="asyncData" :load-node="handleLoad" :expanded-keys="expandedKeys" @expanded="..." />
<l-tree :data="data">
  <template #switcher="{ expanded }">...</template>
  <template #content="{ node }">...</template>
</l-tree>
```

## Props 属性

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| data | 树数据 | Object[] | - |
| keyField, labelField, childrenField, disabledField | 字段名 | string | key/label/children/disabled |
| defaultExpandedKeys, expandedKeys | 默认/受控展开 | (string\|number)[] | - |
| defaultCheckedKeys, checkedKeys | 默认/受控勾选 | (string\|number)[] | - |
| checkable | 显示复选框 | boolean | false |
| cascade | 级联选择 | boolean | false |
| checkStrategy | all/parent/child | string | all |
| checkboxPlacement | left/right | string | left |
| expandOnClick, checkOnClick | 点击展开/勾选 | boolean | false |
| loadNode | 异步加载 (node)=>Promise&lt;boolean&gt; | function | - |
| pattern | 搜索关键词 | string | '' |
| showIrrelevantNodes | 搜索时显示无关节点 | boolean | true |
| allowCheckingNotLoaded | 允许勾选未加载节点 | boolean | false |
| indentWidth | 缩进宽度 | number | 24 |
| center | 节点内容垂直居中 | boolean | false |
| loadingColor, checkedColor | 颜色 | string | - |
| rotatableSwitcher | 展开图标是否旋转 | boolean | false |
| highlightBgColor, selectedBgColor | 高亮/选中背景 | string | - |

## Events 事件

| 名称 | 说明 | 回调 |
|------|------|------|
| update:checked-keys / checked | 勾选变化 | keys |
| update:expanded-keys / expanded | 展开变化 | keys |
| click | 点击节点 | (node, siblings) |

## Slots 插槽

switcher：{ hide, loading, expanded }；content：{ node }。

## 插件标签

- `l-tree`：组件标签
- `lime-tree`：演示标签

## 主题定制

--l-tree-node-*、--l-tree-arrow-*、--l-tree-highlight-bg-color、--l-tree-font-size
