<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
エンティティメンテナンススキル  
===============<!-- /10-Header -->  
<!-- 15-License -->  
[オープン・ライセンス](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MaintenanceSkill/LICENSE.md)  
[文書が自動的に生成される](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
グローバルな記述：**介入に必要なスキル、またはオペレーターが持つスキルを表す。  
バージョン: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## プロパティのリスト  

<sup><sub>[*] 属性に型がない場合は、複数の型があるか、異なるフォーマット/パターンがある可能性があるためです</sub></sup>。  
- `requiredTool[array]`: リストプロパティスキルに必要なツールのリスト。  - `skillDescription[string]`: スキルの説明  - `skillDifficulty[string]`: スキルの難易度  - `skillName[string]`: スキルの名前  - `type[string]`: エンティティのタイプ（MaintenanceSkill）。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
必須プロパティ  
- `id`  - `skillName`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## プロパティのデータモデル記述  
アルファベット順（クリックで詳細表示）  
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
## ペイロードの例  
#### メンテナンススキル NGSI-v2 キー値の例  
以下は、JSON-LD形式のMaintenanceSkillのキー値の例である。これは NGSI-v2 と互換性があり、`options=keyValues` を使用すると個々のエンティティのコンテキストデータを返す。  
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
#### メンテナンススキル NGSI-v2 正規化例  
以下は、正規化された JSON-LD 形式の MaintenanceSkill の例である。これは、オプションを使用しない場合は NGSI-v2 と互換性があり、個々のエンティティのコンテキストデータを返します。  
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
#### メンテナンススキル NGSI-LD キー値の例  
以下は、JSON-LD フォーマットの MaintenanceSkill のキー値の例である。これは NGSI-LD と互換性があり、`options=keyValues` を使用すると個々のエンティティのコンテキストデータを返す。  
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
#### メンテナンススキル NGSI-LD 正規化例  
以下は、正規化された JSON-LD 形式の MaintenanceSkill の例です。これは、オプションを使用しない場合の NGSI-LD と互換性があり、個々のエンティティのコンテキストデータを返します。  
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
マグニチュード単位の扱い方については、[FAQ 10](https://smartdatamodels.org/index.php/faqs/)を参照のこと。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
