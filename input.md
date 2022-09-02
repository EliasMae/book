---
description: 文本输入框
---

# Input

**schema**

```json
{
    "required_flag": 1,
    "required_type": 2,
    "requireRule": {
        "options": [
            {
                "key": "Y12tIYGZpcClZv2z",
                "compare": "eq",
                "category": "1",
                "value": "111",
                "key_obj": {
                    "name": "Y12tIYGZpcClZv2z",
                    "label": "未命名的表单项"
                }
            }
        ],
        "relation": "{0}",
        "message": "特定条件必填提示",
        "relation_str": ""
    },
    "hidden_flag": 2,
    "hidden": 0,
    "disabled": 0,
    "links": [],
    "data_source": 0,
    "data_source_type": 1,
    "source_dict": {},
    "desc_flag": 0,
    "dl_flag": 0,
    "richtip_flag": 0,
    "name": "b3PdVP6Sv2iia1GO",
    "element": "Input",
    "type": "text",
    "label": "未命名的表单项",
    "placeholder": "请输入",
    "activeRule": [],
    "rules": [
        {
            "format": "number",
            "message": "格式错误"
        },
        {
            "min": 2,
            "message": "长度太短"
        },
        {
            "max": 22,
            "message": "超出最大长度"
        }
    ],
    "url": "",
    "parents": [
        "Y12tIYGZpcClZv2z"
    ],
    "decimalDigit": 2
}
```

#### [公共属性](broken-reference)

#### 数字类型

来源：通过校验规则`rules`里的`format=number | money | numberSigned`来进行判断是否要走数字格式化逻辑

数字类型的输入，会在输入过程中把非字符给replace掉

#### decimalDigit

`number`

需要保留的小数位数，前提是数字类型才会进行保留处理。默认为0，-1代表不限制

> ticket 差异字段

**options**

`array`

当此字段有值时，input 允许进入二级页面选择缺省值
