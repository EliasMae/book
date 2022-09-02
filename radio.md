---
description: 单选
---

# Radio

_单选选有三种展示方式，通过`showstyle`进行区分_

#### schema

```json
{
    "required_flag": 1,
    "required_type": 1,
    "requireRule": {
        "options": [
            {
                "key": "",
                "compare": "",
                "category": "1",
                "value": ""
            }
        ],
        "relation": "{0}",
        "message": "",
        "relation_str": ""
    },
    "hidden_flag": 0,
    "hidden": 0,
    "disabled": 0,
    "links": [],
    "data_source": 0,
    "data_source_type": 1,
    "source_dict": {},
    "desc_flag": 1,
    "dl_flag": 1,
    "richtip_flag": 1,
    "name": "Cw3GzcbVURTkEtqh",
    "setName": true,
    "element": "Radio",
    "alias": "",
    "label": "单选",
    "options": [
        {
            "key": "1",
            "label": "笑",
            "value": "1"
        },
        {
            "key": "2",
            "label": "哭",
            "value": "2"
        }
    ],
    "showstyle": "face",
    "defaultValue": "",
    "className": "form-edit-item edit-ing",
    "edit": "1",
    "layout": "vertical",
    "help": "",
    "illustrate": {
        "is_show": false,
        "text": ""
    },
    "filter": false,
    "other": {
        "feedback": "correct"
    },
    "rules": [],
    "subKey": "",
    "parents": [],
    "activeRule": [],
    "url": "",
    "additionAttr": {
        "hiddenAttr": {
            "parent": [],
            "subKey": "",
            "equal": 1,
            "value": "",
            "hidenSwitch": false,
            "hidden_way": 2
        },
        "dataSource": {
            "way": 1,
            "switch": false,
            "url": "",
            "fixed": true,
            "parame": [],
            "subKey": ""
        }
    },
    "hidden_type": 0,
    "back_name": "Cw3GzcbVURTkEtqh",
    "is_new_add": true,
    "desc": "desc",
    "dl": {
        "title": "",
        "type": "ul",
        "subType": "dot",
        "li": [
            "1",
            "2",
            "3"
        ],
        "desc": ""
    },
    "richTip": {
        "title": "ttt",
        "type": "ul",
        "subType": "dot",
        "li": [
            "q",
            "w"
        ],
        "desc": "desc"
    },
    "custom_category_flag": 0
}
```

#### [公共属性](common.md)

#### showstyle

`string`

单选的样式，分三种：

1. square 平行四边形judge；
2. face 表情；
3. normal 普通的选择；

#### options

`Array` key-value形式的对象数组

单选的选项
