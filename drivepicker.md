---
description: 附件选择器
---

# DrivePicker

**schema**

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
    "name": "gS1NF9ega6oVJ7uC",
    "element": "DrivePicker",
    "label": "附件",
    "rules": [
        {
            "message": "必填项",
            "required": 1
        },
        {
            "message": "格式不支持",
            "filetypes": []
        },
        {
            "message": "选择的文件过大，不允许上传",
            "limit": 3
        },
        {
            "message": "选择的文件数量不可超过9个",
            "max": 9
        }
    ],
    "activeRule": [],
    "fileSwitch": true,
    "CustomType": [],
    "typeData": [
        "mpeg4",
        "bmp",
        "gif",
        "png",
        "jpeg"
    ],
    "dataFrom": "camera,album",
    "placeholder": "",
    "defaultValue": "",
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
    },
    "parents": [
        "JQXOBMdcvJeKNVI3"
    ]
}
```

#### [公共属性](broken-reference)

#### dataFrom

`string | string[]`

附件点击相机图标弹框选项，有相册、相机、本地文件、云文件，目前duty暂时只支持相册和相机配置

可以接收`,`分隔的字符串，或者字符串组成的数组

1. album 相册
2. camera 相机拍摄
3. webdisk 云文件
4. shooting 本地文件

#### 附件下方描述

`string`

描述展示的是校验规则rules里的limit项，限制大小的提示

#### 附件最多上传个数

`number`

个数限制取的是 校验规则 rules里的 max项
