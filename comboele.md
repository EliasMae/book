---
description: 时间段选择器
---

# ComboEle

**schema**

```json
{
    "required_flag": 1,
    "required_type": 2,
    "requireRule":
    {
        "options": [
        {
            "key": "JQXOBMdcvJeKNVI3",
            "compare": "neq",
            "category": "1",
            "value": "q",
            "key_obj":
            {
                "name": "JQXOBMdcvJeKNVI3",
                "label": "输入框"
            }
        }],
        "relation": "{0}",
        "message": "日期段必填",
        "relation_str": ""
    },
    "hidden_flag": 0,
    "hidden": 0,
    "disabled": 0,
    "links": [],
    "data_source": 0,
    "data_source_type": 1,
    "source_dict":
    {},
    "desc_flag": 1,
    "dl_flag": 1,
    "richtip_flag": 1,
    "name": "uBN1vEUE5GJXzAdf",
    "element": "DatePicker",
    "type": "DateRange",
    "element_type": "ComboEle",
    "label": "日期",
    "placeholder": "请选择",
    "alias": "",
    "setSwitch": false,
    "rules": [],
    "url": "",
    "parents": [],
    "defaultSwitch": false,
    "defaultValue": "",
    // 开始，结束日期schema
    "schema": [
    {
        "name": "startDate",
        "element": "DatePicker",
        "disabled": 0,
        "rules": [],
        "format": "yyyy-MM-dd  第 w 周",
        "defaultValue": ""
    },
    {
        "name": "endDate",
        "element": "DatePicker",
        "disabled": 0,
        "rules": [],
        "format": "yyyy-MM-dd  第 w 周",
        "defaultValue": ""
    }],
    "activeRule": [],
    "format": "yyyy-MM-dd  第 w 周",
    "desc": "描述",
    "dl":
    {
        "title": "",
        "type": "ul",
        "subType": "dot",
        "li": [
            "1",
            "2"
        ],
        "desc": ""
    },
    "richTip":
    {
        "title": "富文本title",
        "type": "ul",
        "subType": "dot",
        "li": [
            "1",
            "2"
        ],
        "desc": "富文本desc"
    },
    "showRule":
    {
        "options": [
        {
            "key": "",
            "compare": "eq",
            "category": 0,
            "value": ""
        }],
        "relation": "",
        "message": "",
        "relation_str": ""
    }
}
```

#### [公共属性](broken-reference)

#### format

`string`

选择时间段后显示格式，类似 `YYYY/MM/DD HH:mm`

从时间段schema中取，或者时间段schema下的schema中的开始或结束schema中取

#### schema

`schema[]`

存放开始和结束时间的schema的地方，会取里面的name作为提交到后台的key，这俩是平级的单独的

#### 提交格式

组件 onchange 出来的是`13`位数字的时间戳，提交给后台的是`10`位的秒时间戳

同样的接收后台的也是`10`位的秒时间戳，组件接收的是`13`位的数字
