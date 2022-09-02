---
description: 多选
---

# Checkbox

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
    "hidden_flag": 2,
    "hidden": 0,
    "disabled": 0,
    "links": [],
    "data_source": 0,
    "data_source_type": 1,
    "source_dict": {},
    "desc_flag": 1,
    "dl_flag": 1,
    "richtip_flag": 1,
    "name": "bisgVYrIpn5P5PcV",
    "element": "Checkbox",
    "label": "未命名的表单项",
    "alias": "",
    "options": [
        {
            "value": "1",
            "label": "选项1"
        },
        {
            "value": "2",
            "label": "选项2"
        },
        {
            "value": "3",
            "label": "选项3"
        }
    ],
    "defaultValue": {},
    "rules": [
        {
            "min": 2,
            "message": "至少选择 2 项"
        },
        {
            "max": 4,
            "message": "最多选择 4 项"
        }
    ],
    "parents": [],
    "activeRule": [],
    "url": "",
    "desc": "描述",
    "dl": {
        "title": "",
        "type": "ol",
        "subType": "dot",
        "li": [
            "1",
            "2"
        ],
        "desc": ""
    },
    "richTip": {
        "title": "富文本标题",
        "type": "ul",
        "subType": "dot",
        "li": [
            "1",
            "2"
        ],
        "desc": "富文本描述"
    }
}
```

#### [公共属性](broken-reference)

#### options

`Array` key-value形式的对象数组

多选的选项
