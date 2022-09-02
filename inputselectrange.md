---
description: 高级自定义输入组
---

# InputSelectRange

_高级自定义输入组是点击添加后，请求到类别列表，然后跳转到选择类别界面，选择完可以更改类别名称，但是不可与已选择的类别重复；也可以请求外部数据源，然后填充到已选择列表，部分有第三方推送标识_

**schema**

```json
{
    "required_flag": 0,
    "required_type": 2,
    "requireRule": {
        "options": [
            {
                "key": "",
                "compare": "eq",
                "category": 0,
                "value": ""
            }
        ],
        "relation": "",
        "message": "",
        "relation_str": ""
    },
    "hidden_flag": 0,
    "hidden": 1,
    "disabled": 0,
    "links": [
        {
            "type": "form",
            "name": "0324",
            "id": "ROPWBbrvqM5jfTwG"
        },
        {
            "type": "link",
            "link_type": "internal",
            "show_name": "创建任务",
            "link": "123",
            "param": [],
            "params": [
                {
                    "key": "cc",
                    "type": 1,
                    "value": "1234",
                    "desc": "",
                    "required": false
                }
            ]
        }
    ],
    "data_source": 1,
    "data_source_type": 1,
    "source_dict": {},
    "desc_flag": 1,
    "dl_flag": 1,
    "richtip_flag": 1,
    "element": "InputSelectRange",
    "element_type": "InputSelectRange",
    "config": {
        "btnName": "添加",
        "title": "添加输入项",
        "dataSource": "jwBusinessDict",
        "dictId": "Gf9ztbeL2B9fra2jdMfe84JjHROsBU6J"
    },
    "format": "",
    "decimalDigit": 2,
    "extTxt": "刀",
    "defaultValue": "",
    "numberCheck": 1,
    "inputRange": "0,5",
    "inputColor": {
        "in": "20BB7A",
        "out": "FF3B2F"
    },
    "keyMap": {
        "label": "lable",
        "value": "value",
        "type": "type",
        "range": "range",
        "select": "select"
    },
    "label": "日期",
    "name": "PrA8lajkpjECFnmV",
    "rules": [
        {
            "format": "money",
            "message": "格式错误了"
        }
    ],
    "activeRule": [],
    "desc": "描述",
    "dl": {
        "title": "",
        "type": "ul",
        "subType": "dot",
        "li": [
            "1",
            "2"
        ],
        "desc": ""
    },
    "richTip": {
        "title": "富文本title",
        "type": "ul",
        "subType": "dot",
        "li": [
            "1",
            "2"
        ],
        "desc": "富文本desc"
    },
    "parents": [],
    "nextstep_flag": "1",
    "nextstep": {
        "label": "下一步行动标题",
        "options": [
            {
                "label": "走着",
                "value": "",
                "icon": "/openfile/getfile?id=EN4B5a0efzM0LI5C&type=jw_n_image&size=preview"
            },
            {
                "label": "走着2",
                "value": "",
                "icon": "/openfile/getfile?id=5cyQ80oU5Z0tDB6c&type=jw_n_image&size=preview"
            }
        ]
    },
    "third_data_no_del": 1,
    "error_show_links": 1,
    "url": "http://123456.cc",
    "showRule": {
        "options": [
            {
                "key": "",
                "compare": "eq",
                "category": 0,
                "value": ""
            }
        ],
        "relation": "",
        "message": "",
        "relation_str": ""
    }
}
```

#### [公共属性](broken-reference)

#### config

`ConfigType`

输入组添加页面的配置信息

```typescript
type ConfigType = {
    title?: string
    btnName?: string
    dictId?: string
    dataSource?: string
  }
```

1. title 点击添加后跳转到添加类别页面的标题
2. benName 元素下方添加的文本内容
3. dictId 高级输入组用这个来请求类别列表

#### inputRange

`string ,分隔的数字字符`

高级输入组的输入范围，并不是第一级的inputRange，而是根据 dictId 请求到的列表中每项自带的范围。

#### numberCheck

`number`

是否校验输入项是否在配置的 `inputRange` 范围内 1校验 0否

#### inputColor

`InputColorType`

输入组输入内容是否合规的提示颜色，针对输入框的内容

```typescript
type InputColorType = {
  in: string
  out: string
}
```

1. In 符合范围字体色
2. out 超出范围的字体色

#### keyMap

`object`

提交到后台的字段对应的key，由于输入组提交的是一个对象数组，对象的key就是对应 `keyMap` 中的字段

#### extTxt

`string`

输入值的单位，blur时会展示

#### decimalDigit

`number`

保留的数字位数

#### error\_show\_links

`number`

输入组 输入超范围是否展示外链对象 1是 0否

#### nextstep\_flag

`number`

输入超出范围是否有下一步提示 1是 0否

#### nextstep

`NextStepType`

下一步提示内容

```typescript
type NextStepType = {
  label: string
  opitons: StepType[]
}
type StepType = {
  icon: string
  label: string
  value: string
}
```

1. label 下一步弹框提示标题
2. options 下一步弹框提示选项，点击会添加到高级输入组提交数据`select`字段里
   1. Icon 提示图标
   2. label 提示标题
   3. value 提示选中后提交的值

#### data\_source

`number`

是否设置数据来源 1是 0否

#### data\_source\_type

`number`

数据来源，1 自定义数据来源，duty用到的是这个

#### url

`string`

自定义数据来源的数据源链接

**只有data\_source=1 & data\_source\_type=1 & url**时，才会请求外部数据源数据

#### thirdFlag

`number`

第三方推送数据标识

如果请求到的数据中有第三方推送的数据，则不可删除
