# LimeForm 表单

## 介绍

表单组件，支持多种表单项、校验规则(required/pattern/validator 等)、动态表单、布局与对齐、重置/提交/校验。用于登录注册、信息收集、数据提交。**付费组件。**

**依赖：** `lime-shared`、`lime-style`

## 使用

```html
<l-form ref="formRef" :data="formData">
  <l-form-item name="username" label="用户名" :rules="[{ required: true, message: '请填写用户名' }]">
    <l-input v-model="formData.username" placeholder="用户名" :bordered="false" />
  </l-form-item>
  <l-form-item name="password" label="密码" :rules="[{ required: true, message: '请填写密码' }]">
    <l-input v-model="formData.password" type="password" placeholder="密码" :bordered="false" />
  </l-form-item>
  <l-button block type="primary" @click="onSubmit">提交</l-button>
</l-form>
```

## Form Props 属性（节选）

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| data | 表单数据对象 | Object | {} |
| rules | 表单校验规则集 | Object | - |
| layout | horizontal/vertical | string | horizontal |
| labelAlign | start/center/end | string | start |
| labelValign | start/center/end | string | start |
| labelWidth | 标签宽度 | string \| number | 86px |
| asteriskPosition | left/right 星号位置 | string | left |
| disabled / readonly | 禁用/只读整表 | boolean | - |
| requiredMark | 是否显示必填* | boolean | - |
| resetType | empty/initial 重置方式 | string | empty |
| scrollToFirstError | 是否滚动到首个错误 | boolean | true |
| showErrorMessage | 是否显示错误提示 | boolean | true |
| contentAlign | left/right 内容对齐 | string | left |
| errorMessage | 自定义错误文案配置 | FormErrorMessage | - |

## Form Ref 方法

| 名称 | 参数 | 返回值 | 说明 |
|------|------|--------|------|
| validate | (params?: FormValidateParams) | Promise\<Result\> | 校验(带 UI) |
| validateOnly | (params?) | Promise\<Result\> | 静默校验 |
| submit | (params?) | Promise\<UTSJSONObject\> | 提交 |
| reset | (params?: FormResetParams) | void | 重置 |
| clearValidate | (fields?: string[]) | void | 清除校验状态 |
| setValidateMessage | (validateMessages) | void | 设置自定义错误消息 |

## Form Events 事件

| 名称 | 参数 | 说明 |
|------|------|------|
| reset | e: UniFormResetEvent \| null | 表单重置时 |
| submit | { validateResult, firstError } | 提交时 |
| validate | { validateResult } | 任一项校验后 |

## FormItem Props 属性（节选）

| 名称 | 说明 | 类型 | 默认值 |
|------|------|------|--------|
| name | 字段唯一标识 | string | - |
| label | 标签文本 | string | '' |
| rules | 该项校验规则 | Array\<FormRule\> | - |
| help | 说明内容 | string | - |
| arrow | 是否显示右侧箭头 | boolean | false |
| labelWidth / layout / labelAlign / labelValign | 覆盖 Form | string/number | - |
| requiredMark / showErrorMessage | 覆盖 Form | boolean | - |
| bordered | 是否下边框 | boolean | true |
| lStyle / labelStyle | 自定义样式 | string \| object | - |

## FormItem Slots 插槽

| 名称 | 说明 |
|------|------|
| default | 表单项控件 |
| label | 自定义标签 |
| suffix-icon | 后缀图标 |
| message | 提示信息 |

## FormItem Ref 方法

validate、validateOnly、resetField、blur、resetHandler、scrollToField、setValidateMessage

## FormRule 规则（节选）

required、message、trigger(change/blur)、type(error/warning)、min、max、len、pattern、validator、number、boolean、email、url、idcard、telnumber、date、enum、whitespace 等。

## 插件标签

- `l-form`、`l-form-item`：组件标签
- `lime-form`：演示标签

## 主题定制

--l-form-bg-color、--l-form-item-padding-*、--l-form-item-border-*、--l-form-item-label-width、--l-form-item-star-gap
