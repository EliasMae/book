---
description: 块，小节
---

# Section

**Schema**

```json
{
    "addName": "继续添加一组TMD",
    "element": "Section",
    "isAdd": "1",
    "logo": '',
    "name": '',
    "schema": [],
    "splitNodes": []
}
```

#### [公共属性](broken-reference)

#### isAdd

`number`

是否是可添加多组的section 1是 0否

否的话，就是普通的Section，多组另说

#### logo

`string`

section的头部图标

#### label

`string`

section的大标题

#### desc

`string`

为标题label下的描述信息，section没有dl desc等具体表单元素的描述信息

#### schema

`Array`

section下的子元素数组

#### addName

`string`

如果section为可添加多组section，addName为下方的按钮内容

#### name

`string`

普通的section没什么用，多组的name会作为表单数据的key进行提交。

多组的表单数据是一个数组

#### style - marginType

`number`

宽窄边距 0 宽 1窄

#### splitNodes

`string[]`

横向分页的节点，

> 多组的提交
>
> 如果组内有必填项，则添加了多少组就要校验多少组并提交多少组数据；
>
> 如果组内都是非必填项，则只有组内某一项填写了后，才会提交该组数据，否则该组作废
