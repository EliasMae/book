---
description: 时间选择器
---

# DatePicker

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
    "links": [],
    "data_source": 0,
    "data_source_type": 1,
    "source_dict": {},
    "desc_flag": 1,
    "dl_flag": 1,
    "richtip_flag": 1,
    "name": "6OigkBLlMx37nwhL",
    "element": "DatePicker",
    "label": "日期",
    "format": "MM-dd-yyyy  第 w 周",
    "placeholder": "请选择",
    "rules": [
        {
            "maxValue": "+0",
            "message": "不可晚于今天"
        }
    ],
    "parents": [
        "JQXOBMdcvJeKNVI3"
    ],
    "defaultValue": "",
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
        "title": "弹框title",
        "type": "ul",
        "subType": "dot",
        "li": [
            "1",
            "2"
        ],
        "desc": "弹框desc"
    },
    "showRule": {
        "options": [
            {
                "key": "JQXOBMdcvJeKNVI3",
                "compare": "neq",
                "category": "1",
                "value": "11",
                "key_obj": {
                    "name": "JQXOBMdcvJeKNVI3",
                    "label": "输入框"
                }
            }
        ],
        "relation": "{0}",
        "message": "",
        "relation_str": ""
    }
}
```

#### [公共属性](broken-reference)

#### format

`string`

选择时间后显示格式，类似 `YYYY/MM/DD HH:mm`

w代表周有两种显示格式 1：第w周 2：w 2 （第二周）

#### 提交格式

组件onchange出来的是`13`位数字的时间戳，提交给后台的是`10`位的秒时间戳

同样的接收后台的也是`10`位的秒时间戳，组件接收的是`13`位的数字
