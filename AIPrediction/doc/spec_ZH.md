<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
实体：AIPrediction  
===============<!-- /10-Header -->  
<!-- 15-License -->  
[开放许可](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/AIPrediction/LICENSE.md)  
[文件自动生成](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
全局描述：**代表人工智能预测所需的维护干预**  
版本： 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 属性列表  

<sup><sub>[*] 如果属性中没有类型，是因为它可能有多个类型或不同的格式/模式</sub></sup>。  
- `anomalyType[string]`: 异常的类别和等级（分类参照维护）。  - `computedParameters[array]`: ListProperty 属性列表。计算参数列表。  - `country[string]`: 预测相关的国家。  - `date[date]`: 预测日期。  - `exceededThreshold[array]`: 列表属性。已超过的阈值列表。  - `head[string]`: 与头部有关的信息。  - `interventionDuration[integer]`: 干预持续时间（分钟  - `laser[string]`: 激光相关信息。  - `maintenanceTypeBin[string]`: 维护类型的二进制表示。  - `maintenanceTypeDec[integer]`: 维护类型的小数表示法。  - `requiresComponent[array]`: 列表属性。维护所需的机器组件列表。  - `requiresSkill[array]`: ListProperty.所需经验和工具  - `runningTime[integer]`: 运行时间（分钟）。  - `type[string]`: 实体类型（InventoryItem）。  - `weeksForIntervention[integer]`: 干预的最后期限，以周为单位（如果 anomalyClas 为 "完美"，且此值为 52，则实际上无需干预）。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
所需属性  
- `anomalyType`  - `computedParameters`  - `date`  - `exceededThreshold`  - `head`  - `id`  - `interventionDuration`  - `laser`  - `maintenanceTypeBin`  - `maintenanceTypeDec`  - `requiresComponent`  - `requiresSkill`  - `runningTime`  - `type`  - `weeksForIntervention`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 属性的数据模型描述  
按字母顺序排列（点击查看详情）  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
AIPrediction:    
  description: Represent an AI forecasted needed maintenance intervention    
  properties:    
    anomalyType:    
      description: Class and Grade of anomaly (Classification referred to the maintenance).    
      type: string    
      x-ngsi:    
        type: Property    
    computedParameters:    
      description: ListProperty. List of computed parameters.    
      items:    
        description: The computed parameter with its value.    
        properties:    
          name:    
            description: The parameter's name.    
            type: string    
            x-ngsi:    
              type: Property    
          value:    
            description: The value of the parameter.    
            type: number    
            x-ngsi:    
              type: Property    
        type: object    
        x-ngsi:    
          type: Property    
      type: array    
    country:    
      description: The country where the prediction is relevant.    
      type: string    
      x-ngsi:    
        type: Property    
    date:    
      description: The date of the prediction.    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    exceededThreshold:    
      description: ListProperty. List of thresholds that have been exceeded.    
      items:    
        description: The parameter whose threshold has been exceeded.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    head:    
      description: Head-related information.    
      type: string    
      x-ngsi:    
        type: Property    
    interventionDuration:    
      description: Duration of the intervention in minutes    
      type: integer    
      x-ngsi:    
        type: Property    
    laser:    
      description: Laser-related information.    
      type: string    
      x-ngsi:    
        type: Property    
    maintenanceTypeBin:    
      description: Binary representation of the maintenance type.    
      type: string    
      x-ngsi:    
        type: Property    
    maintenanceTypeDec:    
      description: Decimal representation of the maintenance type.    
      type: integer    
      x-ngsi:    
        type: Property    
    requiresComponent:    
      description: ListProperty. List of machine components required for the maintenance.    
      items:    
        description: Required machine components.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    requiresSkill:    
      description: ListProperty. Experience and tools required.    
      items:    
        description: Technical skill description.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    runningTime:    
      description: Running time in minutes.    
      type: integer    
      x-ngsi:    
        type: Property    
    type:    
      description: The type of the entity (InventoryItem).    
      type: string    
      x-ngsi:    
        type: Property    
    weeksForIntervention:    
      description: Deadline for intervention, in weeks (if anomalyClas is 'Perfect' and this is 52, no intervention is actually required).    
      type: integer    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - date    
    - laser    
    - head    
    - runningTime    
    - computedParameters    
    - anomalyType    
    - weeksForIntervention    
    - exceededThreshold    
    - maintenanceTypeBin    
    - maintenanceTypeDec    
    - requiresSkill    
    - requiresComponent    
    - interventionDuration    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/AIPrediction/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/AIPrediction/schema.json    
  x-model-tags: maintenance    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## 有效载荷示例  
#### AIPrediction NGSI-v2 键值示例  
下面是一个以 JSON-LD 格式作为键值的 AIPrediction 示例。当使用 `options=keyValues` 时，它与 NGSI-v2 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/AIPrediction/aiPrediction01",  
    "type": "AIPrediction",  
    "country": "Italy",  
    "date": "25/12/2025",  
    "laser": "YLS6000",  
    "head": "T5-Precitec",  
    "runningTime": 1411,  
    "computedParameters": [  
        {  
            "name": "param00",  
            "value": 0.0  
        },  
        {  
            "name": "param01",  
            "value": 0.0  
        },  
        {  
            "name": "param02",  
            "value": 0.0  
        },  
        {  
            "name": "param03",  
            "value": 0.0  
        },  
        {  
            "name": "param04",  
            "value": 0.0  
        },  
        {  
            "name": "param05",  
            "value": 0.0  
        },  
        {  
            "name": "param06",  
            "value": 0.0  
        },  
        {  
            "name": "param07",  
            "value": 1.0  
        },  
        {  
            "name": "param08",  
            "value": 0.0  
        },  
        {  
            "name": "param09",  
            "value": 1.0  
        },  
        {  
            "name": "param10",  
            "value": 1.0  
        },  
        {  
            "name": "param11",  
            "value": 0.0  
        },  
        {  
            "name": "param12",  
            "value": 1.0  
        },  
        {  
            "name": "param13",  
            "value": 0.0  
        }  
    ],  
    "anomalyType": "Near To Fail",  
    "weeksForIntervention": 1,  
    "exceededThreshold": [  
        "Param07",  
        "Param09",  
        "Param10",  
        "Param_12"  
    ],  
    "maintenanceTypeBin": "1011",  
    "maintenanceTypeDec": 11,  
    "requiresSkill": [  
        "MaintenanceSkill:maintenanceSkill01"  
    ],  
    "requiresComponent": [  
        "MachineComponent:machineComponent01"  
    ],  
    "interventionDuration": 19  
}  
```  
</details>  
#### AIPrediction NGSI-v2 标准化示例  
下面是一个规范化 JSON-LD 格式的 AIPrediction 示例。当不使用选项时，它与 NGSI-v2 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:AIPrediction:aiPrediction01",  
    "type": "AIPrediction",  
    "country": {  
        "type": "Property",  
        "value": "Italy"  
    },  
    "date": {  
        "type": "Property",  
        "value": "2025-12-25"  
    },  
    "laser": {  
        "type": "Property",  
        "value": "YLS6000"  
    },  
    "head": {  
        "type": "Property",  
        "value": "T5-Precitec"  
    },  
    "runningTime": {  
        "type": "Property",  
        "value": 1411  
    },  
    "computedParameters": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param00"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param01"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param02"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param03"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param04"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param05"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param06"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param07"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param08"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param09"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param10"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param11"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param12"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param13"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            }  
        ]  
    },  
    "anomalyType": {  
        "type": "Property",  
        "value": "Near To Fail"  
    },  
    "weeksForIntervention": {  
        "type": "Property",  
        "value": 1  
    },  
    "exceededThreshold": {  
        "type": "ListProperty",  
        "value": [  
            "param07",  
            "param09",  
            "param10",  
            "param12"  
        ]  
    },  
    "maintenanceTypeBin": {  
        "type": "Property",  
        "value": "1011"  
    },  
    "maintenanceTypeDec": {  
        "type": "Property",  
        "value": 11  
    },  
    "requiresSkill": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MaintenanceSkill:maintenanceSkill01"  
            }  
        ]  
    },  
    "requiresComponent": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MaintenanceComponent:maintenanceComponent01"  
            }  
        ]  
    },  
    "interventionDuration": {  
        "type": "Property",  
        "value": 19  
    }  
}  
```  
</details>  
#### AIPrediction NGSI-LD 键值示例  
下面是一个以 JSON-LD 格式作为键值的 AIPrediction 示例。当使用 `options=keyValues` 时，它与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/AIPrediction/aiPrediction01",  
    "type": "AIPrediction",  
    "country": "Italy",  
    "date": "2025-12-25",  
    "laser": "YLS6000",  
    "head": "T5-Precitec",  
    "runningTime": 1411,  
    "computedParameters": [  
        {  
            "name": "param00",  
            "value": 0.0  
        },  
        {  
            "name": "param01",  
            "value": 0.0  
        },  
        {  
            "name": "param02",  
            "value": 0.0  
        },  
        {  
            "name": "param03",  
            "value": 0.0  
        },  
        {  
            "name": "param04",  
            "value": 0.0  
        },  
        {  
            "name": "param05",  
            "value": 0.0  
        },  
        {  
            "name": "param06",  
            "value": 0.0  
        },  
        {  
            "name": "param07",  
            "value": 1.0  
        },  
        {  
            "name": "param08",  
            "value": 0.0  
        },  
        {  
            "name": "param09",  
            "value": 1.0  
        },  
        {  
            "name": "param10",  
            "value": 1.0  
        },  
        {  
            "name": "param11",  
            "value": 0.0  
        },  
        {  
            "name": "param12",  
            "value": 1.0  
        },  
        {  
            "name": "param13",  
            "value": 0.0  
        }  
    ],  
    "anomalyType": "Near To Fail",  
    "weeksForIntervention": 1,  
    "exceededThreshold": [  
        "Param07",  
        "Param09",  
        "Param10",  
        "Param_12"  
    ],  
    "maintenanceTypeBin": "1011",  
    "maintenanceTypeDec": 11,  
    "requiresSkill": [  
        "MaintenanceSkill:maintenanceSkill01"  
    ],  
    "requiresComponent": [  
        "MachineComponent:machineComponent01"  
    ],  
    "interventionDuration": 19  
}  
```  
</details>  
#### AIPrediction NGSI-LD normalized 示例  
下面是一个规范化 JSON-LD 格式的 AIPrediction 示例。当不使用选项时，它与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/AIPrediction/aiPrediction01",  
    "type": "AIPrediction",  
    "country": {  
        "type": "Property",  
        "value": "Italy"  
    },  
    "date": {  
        "type": "Property",  
        "value": "2025-12-25"  
    },  
    "laser": {  
        "type": "Property",  
        "value": "YLS6000"  
    },  
    "head": {  
        "type": "Property",  
        "value": "T5-Precitec"  
    },  
    "runningTime": {  
        "type": "Property",  
        "value": 1411  
    },  
    "computedParameters": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param00"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param01"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param02"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param03"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param04"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param05"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param06"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param07"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param08"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param09"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param10"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param11"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param12"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param13"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            }  
        ]  
    },  
    "anomalyType": {  
        "type": "Property",  
        "value": "Near To Fail"  
    },  
    "weeksForIntervention": {  
        "type": "Property",  
        "value": 1  
    },  
    "exceededThreshold": {  
        "type": "Property",  
        "value": [  
            "Param07",  
            "Param09",  
            "Param10",  
            "Param_12"  
        ]  
    },  
    "maintenanceTypeBin": {  
        "type": "Property",  
        "value": "1011"  
    },  
    "maintenanceTypeDec": {  
        "type": "Property",  
        "value": 11  
    },  
    "requiresSkill": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MaintenanceSkill:maintenanceSkill01"  
            }  
        ]  
    },  
    "requiresComponent": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MachineComponent:machineComponent01"  
            }  
        ]  
    },  
    "interventionDuration": {  
        "type": "Property",  
        "value": 19  
    }  
}  
```  
</details><!-- /80-Examples -->  
<!-- 90-FooterNotes -->  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
请参阅 [FAQ 10](https://smartdatamodels.org/index.php/faqs/)，获取如何处理幅度单位的答案。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
