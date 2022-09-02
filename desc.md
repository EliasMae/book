---
description: 描述
---

# Desc

_Desc 是一个单独的展示组件，可以配一些描述或者结构描述信息，不产生表单信息。也可以配置特定条件下展示_

**Schema**

```json
{
    "required_flag": 2,
    "required_type": 1,
    "hidden_flag": 1,
    "hidden": 0,
    "disabled": 0,
    "links": [],
    "data_source": 0,
    "data_source_type": 1,
    "source_dict": {},
    "desc_flag": 1,
    "dl_flag": 1,
    "richtip_flag": 0,
    "label": "未命名的表单项",
    "element_type": "Desc",
    "element": "Custom",
    "name": "j5LWZgOmmrOr7niD",
    "rules": [],
    "activeRule": [],
    "desc": "描述",
    "dl": {
        "title": "",
        "type": "ul",
        "subType": "dot",
        "li": [
            "结构1",
            "结构2",
            "结构3"
        ],
        "desc": ""
    },
    "showRule": {
        "options": [
            {
                "key": "nU4J5ON3rnlAZuGo",
                "compare": "eq",
                "category": "1",
                "value": "111",
                "key_obj": {
                    "name": "nU4J5ON3rnlAZuGo",
                    "label": "输入框"
                }
            }
        ],
        "relation": "{0}",
        "message": "",
        "relation_str": ""
    },
    "parents": [
        "nU4J5ON3rnlAZuGo"
    ]
}
```

#### [公共属性](broken-reference)

#### 最大输入长度

根据校验规则rules里的 max 进行限制，过长不可再输入
