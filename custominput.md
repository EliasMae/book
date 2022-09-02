---
description: 自定义输入组
---

# CustomInput

_点击添加后，会跳转到输入类别界面，两次添加不可重复_

**schema**

```json
{
    "required_flag": 1,
    "required_type": 1,
    "requireRule": {
        "options": [],
        "relation": "",
        "message": "",
        "relation_str": ""
    },
    "hidden_flag": 1,
    "hidden": 0,
    "disabled": 0,
    "links": [
        {
            "type": "link",
            "link_type": "internal",
            "show_name": "创建任务",
            "link": "12345",
            "param": []
        },
        {
            "type": "form",
            "name": "0324",
            "id": "ROPWBbrvqM5jfTwG"
        }
    ],
    "data_source": 0,
    "data_source_type": 1,
    "source_dict": {},
    "desc_flag": 1,
    "dl_flag": 1,
    "richtip_flag": 1,
    "name": "yFZBrf8vj37z5hEU",
    "other": {},
    "element_type": "CustomInput",
    "element": "CustomInput",
    "config": {
        "btnName": "添加",
        "title": "添加输入项",
        "dataSource": "jwBusinessDict",
        "dictId": "77",
        "dictName": "业务字典5"
    },
    "rules": [
        {
            "format": "number",
            "message": "格式错误"
        }
    ],
    "format": "",
    "decimalDigit": 2,
    "extTxt": "个",
    "defaultValue": [],
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
    "label": "自定义输入组",
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
    "error_show_links": 1,
    "showRule": {
        "options": [
            {
                "key": "JQXOBMdcvJeKNVI3",
                "compare": "eq",
                "category": "1",
                "value": "2",
                "key_obj": {
                    "name": "JQXOBMdcvJeKNVI3",
                    "label": "输入框"
                }
            }
        ],
        "relation": "{0}",
        "message": "",
        "relation_str": ""
    },
    "parents": [
        "JQXOBMdcvJeKNVI3"
    ]
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
3. dictId 用于获取输入历史的id，添加类别页面在输入过程中会匹配输入记录，提交后会保存本次输入

#### inputRange

`string ,分隔的数字字符`

输入组的输入范围

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
