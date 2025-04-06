<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
实体：任命  
=====<!-- /10-Header -->  
<!-- 15-License -->  
[开放许可](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/Appointment/LICENSE.md)  
[文件自动生成](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
全球描述：**代表操作员的预约**  
版本： 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 属性列表  

<sup><sub>[*] 如果属性中没有类型，是因为它可能有多个类型或不同的格式/模式</sub></sup>。  
- `appointmentDescription[string]`: 任命说明。  - `category[string]`: 任命类别。  - `externalKey[array]`: 列表属性。该元素的外部键。  - `flag[string]`: 任命的旗帜。  - `from[date]`: 预约的开始日期和时间。  - `note[string]`: 约会补充说明。  - `recurring[boolean]`: 表示预约是否重复。  - `recurringException[string]`: 任命的经常性例外情况。  - `recurringRule[string]`: 任命的经常性规则。  - `to[date]`: 预约的结束日期和时间。  - `type[string]`: 实体类型（InventoryItem）。  - `wholeDay[boolean]`: 表示预约是否为全天活动。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
所需属性  
- `appointmentDescription`  - `category`  - `externalKey`  - `from`  - `id`  - `recurring`  - `to`  - `type`  - `wholeDay`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 属性的数据模型描述  
按字母顺序排列（点击查看详情）  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
Appointment:    
  description: Represent an scheduled appointment for the operator    
  properties:    
    appointmentDescription:    
      description: The description of the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    category:    
      description: The category of the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    externalKey:    
      description: ListProperty. The external keys for this element.    
      items:    
        description: The external key for this element.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    flag:    
      description: The flag for the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    from:    
      description: The start date and time of the appointment.    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    note:    
      description: Additional notes for the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    recurring:    
      description: Indicates if the appointment is recurring.    
      type: boolean    
      x-ngsi:    
        type: Property    
    recurringException:    
      description: The recurring exception for the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    recurringRule:    
      description: The recurring rule for the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    to:    
      description: The end date and time of the appointment.    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: The type of the entity (InventoryItem).    
      type: string    
      x-ngsi:    
        type: Property    
    wholeDay:    
      description: Indicates if the appointment is a whole day event.    
      type: boolean    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - externalKey    
    - from    
    - to    
    - wholeDay    
    - recurring    
    - category    
    - appointmentDescription    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/Appointment/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/Appointment/schema.json    
  x-model-tags: maintenance    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## 有效载荷示例  
#### 预约 NGSI-v2 密钥值示例  
下面是一个以 JSON-LD 格式作为键值的预约示例。当使用 `options=keyValues` 时，这与 NGSI-v2 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/Appointment/appointment01",  
    "type": "Appointment",  
    "externalKey": [  
        "F105024",  
        "0000000000 970"  
    ],  
    "from": "2024-08-12",  
    "to": "2024-08-14",  
    "wholeDay": true,  
    "recurring": false,  
    "category": "808080",  
    "appointmentDescription": "EX_Ferie  NO PRESIDIO U-FORM"  
}  
```  
</details>  
#### 预约 NGSI-v2 标准化示例  
下面是一个规范化 JSON-LD 格式的 "任命 "示例。在不使用选项的情况下，它与 NGSI-v2 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:Appointment:appointment01",  
    "type": "Appointment",  
    "externalKey": {  
        "type": "Property",  
        "value": [  
            "F105024",  
            "0000000000 970"  
        ]  
    },  
    "from": {  
        "type": "Property",  
        "value": "2024-08-12"  
    },  
    "to": {  
        "type": "Property",  
        "value": "2024-08-14"  
    },  
    "wholeDay": {  
        "type": "Property",  
        "value": true  
    },  
    "recurring": {  
        "type": "Property",  
        "value": false  
    },  
    "category": {  
        "type": "Property",  
        "value": "808080"  
    },  
    "appointmentDescription": {  
        "type": "Property",  
        "value": "EX_Ferie  NO PRESIDIO U-FORM"  
    }  
}  
```  
</details>  
#### 预约 NGSI-LD 键值 示例  
下面是一个以 JSON-LD 格式作为键值的预约示例。当使用 `options=keyValues` 时，这与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/Appointment/appointment01",  
    "type": "Appointment",  
    "externalKey": [  
        "F105024",  
        "0000000000 970"  
    ],  
    "from": "2024-08-12",  
    "to": "2024-08-14",  
    "wholeDay": true,  
    "recurring": false,  
    "category": "808080",  
    "appointmentDescription": "EX_Ferie  NO PRESIDIO U-FORM"  
}  
```  
</details>  
#### 预约 NGSI-LD 正常化示例  
下面是一个规范化 JSON-LD 格式的预约示例。当不使用选项时，它与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/Appointment/appointment01",  
    "type": "Appointment",  
    "externalKey": {  
        "type": "Property",  
        "value": [  
            "F105024",  
            "0000000000 970"  
        ]  
    },  
    "from": {  
        "type": "Property",  
        "value": "2024-08-12"  
    },  
    "to": {  
        "type": "Property",  
        "value": "2024-08-14"  
    },  
    "wholeDay": {  
        "type": "Property",  
        "value": true  
    },  
    "recurring": {  
        "type": "Property",  
        "value": false  
    },  
    "category": {  
        "type": "Property",  
        "value": "808080"  
    },  
    "appointmentDescription": {  
        "type": "Property",  
        "value": "EX_Ferie  NO PRESIDIO U-FORM"  
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
