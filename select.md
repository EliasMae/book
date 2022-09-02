---
description: 下拉选择器
---

# Select

**schema**

```json
{
    "required_flag": 1,
    "required_type": 2,
    "requireRule": {
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
        "message": "输入框值为1时，多行必填",
        "relation_str": ""
    },
    "hidden_flag": 1,
    "hidden": 0,
    "disabled": 0,
    "links": [],
    "data_source": 0,
    "data_source_type": 1,
    "desc_flag": 1,
    "dl_flag": 1,
    "richtip_flag": 1,
    "name": "HTxtHKlOfPhxne8U",
    "element": "Select",
    "label": "多行",
    "placeholder": "请选择",
    "defaultValue": {
        "value": "1",
        "label": "选项1"
    },
    "options": [
        {
            "value": "-0",
            "label": "请选择"
        },
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
    "activeRule": [],
    "rules": [],
    "url": "",
    "parents": [
        "JQXOBMdcvJeKNVI3"
    ],
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
    "custom_category_flag": 1,
    "custom_category_options": [
        "2"
    ],
    "custom_category": {
        "name": "111",
        "tip_flag": 1,
        "tip_content": "这是分类提示",
        "tip_color": "FF3B2F"
    },
    "showRule": {
        "options": [
            {
                "key": "JQXOBMdcvJeKNVI3",
                "compare": "neq",
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

#### options

`Array` key-value形式的对象数组

下拉选择的选项

#### 提交格式

提交后台的格式是 options中的某个对象
