<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
エンティティ任命  
========<!-- /10-Header -->  
<!-- 15-License -->  
[オープン・ライセンス](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/Appointment/LICENSE.md)  
[文書は自動的に生成される](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
グローバルな説明**オペレータの予定されたアポイントメントを表す。  
バージョン: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## プロパティのリスト  

<sup><sub>[*] 属性に型がない場合は、複数の型があるか、異なるフォーマット/パターンがある可能性があるためです</sub></sup>。  
- `appointmentDescription[string]`: 任命の説明。  - `category[string]`: 任命のカテゴリー。  - `externalKey[array]`: ListProperty。この要素の外部キー。  - `flag[string]`: 任命の旗。  - `from[date]`: 予約の開始日時。  - `note[string]`: アポイントに関する補足事項  - `recurring[boolean]`: 予約が定期的かどうかを示します。  - `recurringException[string]`: 再三にわたる例外的な起用。  - `recurringRule[string]`: 起用規則の繰り返し。  - `to[date]`: アポイントメントの終了日時。  - `type[string]`: エンティティのタイプ（InventoryItem）。  - `wholeDay[boolean]`: アポイントメントが終日イベントであるかどうかを示します。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
必須プロパティ  
- `appointmentDescription`  - `category`  - `externalKey`  - `from`  - `id`  - `recurring`  - `to`  - `type`  - `wholeDay`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## プロパティのデータモデル記述  
アルファベット順（クリックで詳細表示）  
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
## ペイロードの例  
#### NGSI-v2 のキー値例  
以下は、JSON-LD形式のkey-valuesとしてのAppointmentの例である。これはNGSI-v2と互換性があり、`options=keyValues`を使用すると、個々のエンティティのコンテキストデータを返す。  
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
#### NGSI-v2を正規化した例  
以下は、正規化されたJSON-LD形式のAppointmentの例である。これは、オプションを使用しない場合、NGSI-v2と互換性があり、個々のエンティティのコンテキストデータを返します。  
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
#### NGSI-LDのキー値例  
以下は、JSON-LD形式のAppointmentをkey-valuesとした例である。options=keyValues`を使うとNGSI-LDと互換性があり、個々のエンティティのコンテキストデータを返す。  
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
#### NGSI-LDを正規化した例  
以下は、正規化されたJSON-LD形式のAppointmentの例である。これは、オプションを使用しない場合はNGSI-LDと互換性があり、個々のエンティティのコンテキストデータを返します。  
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
マグニチュード単位の扱い方については、[FAQ 10](https://smartdatamodels.org/index.php/faqs/)を参照のこと。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
