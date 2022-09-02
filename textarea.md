---
description: 文本域(多行文本)
---

# Textarea

_Textarea 在 Duty2.0 中，是一行的形式展示_

#### schema

```json
{
    "required_flag": 2,
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
    "name": "EGvl389bnU7J78o2",
    "element": "Textarea",
    "type": "textarea",
    "label": "多行",
    "placeholder": "请输入",
    "defaultValue": "fff",
    "activeRule": [],
    "rules": [
        {
            "min": 1,
            "message": "太少了"
        },
        {
            "max": 20,
            "message": "太长了"
        }
    ],
    "url": "",
    "parents": [
        "JQXOBMdcvJeKNVI3"
    ],
    "desc": "描述信息",
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
    "showRule": {
        "options": [
            {
                "key": "JQXOBMdcvJeKNVI3",
                "compare": "eq",
                "category": "1",
                "value": "1",
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

#### 最大输入长度

根据校验规则rules里的 max 进行限制，过长不可再输入
