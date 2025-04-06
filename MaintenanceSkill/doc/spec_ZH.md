<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
实体：维护技能  
=======<!-- /10-Header -->  
<!-- 15-License -->  
[开放许可](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MaintenanceSkill/LICENSE.md)  
[文件自动生成](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
全局描述：**代表干预所需的技能或操作员拥有的技能**  
版本： 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 属性列表  

<sup><sub>[*] 如果属性中没有类型，是因为它可能有多个类型或不同的格式/模式</sub></sup>。  
- `requiredTool[array]`: 列表属性。该技能所需的工具列表。  - `skillDescription[string]`: 技能描述  - `skillDifficulty[string]`: 技能难度。  - `skillName[string]`: 技能名称。  - `type[string]`: 实体类型（MaintenanceSkill）。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
所需属性  
- `id`  - `skillName`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 属性的数据模型描述  
按字母顺序排列（点击查看详情）  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
MaintenanceSkill:    
  description: Represent a skill required for an intervention or possessed by an operator    
  properties:    
    requiredTool:    
      description: ListProperty. List of tools required for the skill.    
      items:    
        description: Name of the required tool.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    skillDescription:    
      description: Description of the skill.    
      type: string    
      x-ngsi:    
        type: Property    
    skillDifficulty:    
      description: Difficulty of the skill.    
      type: string    
      x-ngsi:    
        type: Property    
    skillName:    
      description: Name of the skill.    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: The type of the entity (MaintenanceSkill).    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - skillName    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/MaintenanceSkill/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceSkill/schema.json    
  x-model-tags: maintenace    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## 有效载荷示例  
#### MaintenanceSkill NGSI-v2 key-values 示例  
下面是一个以 JSON-LD 格式作为键值的 MaintenanceSkill 示例。当使用 `options=keyValues` 时，它与 NGSI-v2 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:MaintenanceSkill:maintenanceSkill01",  
    "type": "MaintenanceSkill",  
    "skillName": "Engine Repair",  
    "skillDifficulty": "Advanced",  
    "skillDescription": "This skill involves diagnosing and repairing engine issues in vehicles.",  
    "requiredTool": [  
        "Wrench Set",  
        "Socket Set",  
        "OBD-II Scanner",  
        "Jack and Jack Stands"  
    ]  
}  
```  
</details>  
#### 维护技能 NGSI-v2 标准化示例  
下面是一个规范化 JSON-LD 格式的 MaintenanceSkill 示例。在不使用选项时，它与 NGSI-v2 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:MaintenanceSkill:maintenanceSkill01",  
    "type": "MaintenanceSkill",  
    "skillName": {  
        "type": "Text",  
        "value": "Engine Repair"  
    },  
    "skillDifficulty": {  
        "type": "Text",  
        "value": "Advanced"  
    },  
    "skillDescription": {  
        "type": "Text",  
        "value": "This skill involves diagnosing and repairing engine issues in vehicles."  
    },  
    "requiredTool": {  
        "type": "Text",  
        "value": [  
            "Wrench Set",  
            "Socket Set",  
            "OBD-II Scanner",  
            "Jack and Jack Stands"  
        ]  
    }  
}  
```  
</details>  
#### 维护技能 NGSI-LD 关键值示例  
下面是一个以 JSON-LD 格式作为键值的 MaintenanceSkill 示例。当使用 `options=keyValues` 时，它与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceSkill/maintenanceSkill01",  
    "type": "MaintenanceSkill",  
    "skillName": "Engine Repair",  
    "skillDifficulty": "Advanced",  
    "skillDescription": "This skill involves diagnosing and repairing engine issues in vehicles.",  
    "requiredTool": [  
        "Wrench Set",  
        "Socket Set",  
        "OBD-II Scanner",  
        "Jack and Jack Stands"  
    ]  
}  
```  
</details>  
#### 维护技能 NGSI-LD 标准化示例  
下面是一个规范化 JSON-LD 格式的 MaintenanceSkill 示例。在不使用选项时，它与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "type": "MaintenanceSkill",  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceSkill/maintenanceSkill01",  
    "skillName": {  
        "type": "Property",  
        "value": "Engine Repair"  
    },  
    "skillDifficulty": {  
        "type": "Property",  
        "value": "Advanced"  
    },  
    "skillDescription": {  
        "type": "Property",  
        "value": "This skill involves diagnosing and repairing engine issues in vehicles."  
    },  
    "requiredTool": {  
        "type": "ListProperty",  
        "value": [  
            "Wrench Set",  
            "Socket Set",  
            "OBD-II Scanner",  
            "Jack and Jack Stands"  
        ]  
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
