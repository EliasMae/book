---
description: 公共属性
---

# Common

**schema**

```json
{
    "name": "SjXR3z83zyzDU1FQ",
    "label": "文本",
    "hidden": 0,
    "disabled": 0,
    "required_flag": 2,
    "placeholder": "请输入",
    "desc_flag": 0,
    "desc": "",
    "dl_flag": 0,
    "dl": {
        "li": [
            "2",
            "3"
        ],
        "desc": "",
        "type": "ul",
        "title": "",
        "subType": "dot"
    },
    "richtip_flag": 1,
    "richtip": {
        "li": [
            "1",
            "2"
        ],
        "desc": "rich desc",
        "type": "ol",
        "title": "title",
        "subType": "dot"
    },
    "parents": [
        "4lFS3W6LwWJjYzWZ"
    ],
    "showRule": {
        "message": "",
        "options": [
            {
                "key": "4lFS3W6LwWJjYzWZ",
                "value": "1648791814",
                "compare": "eq",
                "category": "3"
            }
        ],
        "relation": "{0}"
    },
    "links": [
        {
            "link": "ffs",
            "type": "link",
            "param": [],
            "params": [
                {
                    "key": "s",
                    "desc": "",
                    "type": 1,
                    "value": "ddd",
                    "required": false
                }
            ],
            "link_type": "internal",
            "show_name": "发发发"
        },
        {
            "id": "NXKsaEMlfUqfOGZo",
            "name": "多组",
            "type": "form"
        }
    ]
}
```

#### element

元素类型

| element | Input | Textarea | Checkbox                                            | Radio | DatePicker | ComboEle         | ExtraBtn | Select | Desc | DrivePicker | CustomInput | InputSelectRange | Section          |
| ------- | ----- | -------- | --------------------------------------------------- | ----- | ---------- | ---------------- | -------- | ------ | ---- | ----------- | ----------- | ---------------- | ---------------- |
| 元素      | 输入框   | 多行文本     | 多选                                                  | 单选    | 时间选择器      | 时间段选择            | 外链对象     | 下拉选择   | 描述组件 | 附件          | 自定义输入组      | 高级自定义输入组         | 块                |
| 说明      | 普通/数字 |          | showstyle展示样式 ：normal正常 ；square类似judgeRadio ；face笑脸 |       |            | 提交的是两个单独字段：开始+结束 | 匹配links  |        |      |             |             |                  | 通过isAdd区分是否可添加多组 |

#### label

`string`

元素的标题

#### name

`string`

元素的唯一标识，提交表单数据的key

#### defaultValue

`any`

元素默认值， 区分元素类型

#### disabled

`number`

元素是否是不可操作状态 1: true 0: false

#### hidden

`number`

是否无条件隐藏 1是 | 0否

#### required\_flag

`number`

是否必填标识： 1必填 0非必填

#### placeholder

`string`

Input textarea select的占位符

#### desc\_flag

`number`

是否展示元素描述标识 1是 0否

#### desc

`string`

元素描述内容

#### dl\_flag

`number`

是否展示结构化描述 1是 0否

#### dl

`DlType`

元素结构化描述内容

```typescript
type DlType = {
  li: string[]
  desc: string
  title: string
  subType: "circle" | "dot"
  type: "ol" | "ul"
}
```

**li**

`string[]`

结构化描述列表(有序|无序)的每项

**desc**

`string`

只有在元素右侧有富文本提示的时候用到desc，富文本描述

**title**

`string`

只有在元素右侧有富文本提示的时候用到title，富文本标题

**subType**

`string`

无序列表的序号占位-结构化描述的 circle: 圆圈 | dot: 实心黑圆

**type**

`string`

ol: 有序列表 ul: 无序列表

#### richtip\_flag

`number`

富文本展示标识 1是 | 0否

展示的话 会在元素标题右侧有一个tips， 点击会弹框提示 **richtip** 的内容

#### richtip

`DlType`

富文本提示内容

#### parents

`String[]`

订阅的其他元素，会监听parents里的元素的变动，进而更新本元素

showRule 规则里的元素name也需要包含在内，

#### showRule

`RulesType`

特定条件下显示规则：默认隐藏，只有满足showRule条件规则后，才会展示

```typescript
interface RulesType {
  options?: RulesOptionsType[]
  relation?: string
}

interface RulesOptionsType {
  key: string
  compare: string
  value: string
}
```

1. key 每个比较项监听的元素name
2. compare 比对计算符 `eq`:等于; `neq`:不等于; `gt`: 大于; `lt`: 小于; `egt`: 不大于; `elt`: 不小于; _---王奇_
3. value 比较的目标值 如：等于2
4. relation 一个或多个元素的计算公式 如：`{0}and{1}` 则计算options里的第1、2项是否同时满足

#### links

`LinkType`

元素下展示外链对象的内

```typescript
type LinkType = LinksType[]

type LinksType = {
  /**
   * 外联类型
   */
  type: "form" | "link"
  /**
   * type = form时下发的表单id
   */
  id: string
  /**
   * 名字
   */
  name: string

  /**
   * type = link时下发
   * 显示文本
   */
  show_name: string
  /**
   * type = link时下发
   * link链接
   */
  link: string
  desc?: string
  /**
   * type = link时下发
   * external 跳转webview
   * internal 走内部jw协议
   */
  link_type: "external" | "internal"
  /**
   * type = link时下发
   */
  params: {
    /**
     * 参数值类型 1自定义 2选项值 3系统变量
     */
    type: 1 | 2 | 3
    key: string
    value: any
  }[]
}
```

1. type 外链对象类型 `form`:挂的表单; `link`: 链接; 链接分外部链接和内部链接
2. id `type=form`时，下发的表单id
3. name `type=form`时，下发的表单名称
4. show\_name `type=link`时，下发的链接名称
5. link\_type 链接类型，`external`外部H5链接，`internal` 内部链接跳转到创建任务，会通过`params`带三种参数过去
6. link type=link时，下发的链接地址，duty中当`link_type=external`外部链接时，会用到该地址
7. params `type=link & link_type=internal`时，会跳转创建任务，带三种类型值过去
   1. type `1`: 自定义; `2`: 表单选项值; `3`: 系统上下文的值， 如用户名称等;
   2. value type值是`1`: 自定义值; `2`: 表单选项的name; `3`: 系统上下文取值，如`{jw.user.id}`

#### requireRule

`RulesType`

条件必填规则，满足特定条件时，该项才会是必填，类型参考[条件显示](common.md#showrule)

#### rules

`RuleType`

校验规则

```typescript
type RuleType = RulesType[]

type RulesType = {
  format?: 'number' | 'money' | 'numberSigned' | 'email' | 'mobile'
  min?: number
  max?: number
  limit?: number
  minValue?: number  
  maxValue?: number
  message?: string
}
```

1. format 校验格式
2. limit 附件的最大上传大小
3. min | max 长度限制，如果目标对象的值是数组会比较值的length
4. maxValue | minValue 最大最小值限制
   1. 日期minValue='+0'：不可早于今天
   2. 日期maxValue="+0"：不可晚于今天
5. message 错误提示

#### custom\_category\_flag

`number`

是否显示表单题型自定义分类，1是 0否

#### custom\_category\_options

`string[] | object`

关联表单题型自定义分类，当元素选择里面的特定值时，显示 `custom_category`的提示内容

#### custom\_category

`CategoryType`

```typescript
type CategoryType = {
  name: string
  tip_color: string
  tip_content: string
}
```

1. name 自定义分类的名称
2. tip\_color 提示内容的颜色
3. tip\_content 提示内容

> ticket 差异字段

**disabled**

`number`

可选值 0/1/2

是否不可操作状态，当 = 2 时，表示若当前 input 有默认值，则不允许编辑；若为空，则允许编辑

**needSubmit**

`boolean`

可选值 true/false

当 hidden = 1 时，Web 端需要以此字段来判断是否需要提交该元素
