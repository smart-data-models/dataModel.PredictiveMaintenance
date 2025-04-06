<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
エンティティAIPrediction（予測  
=====================<!-- /10-Header -->  
<!-- 15-License -->  
[オープン・ライセンス](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/AIPrediction/LICENSE.md)  
[文書が自動的に生成される](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
グローバルな説明**AIが予測した必要なメンテナンス介入を表す**。  
バージョン: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## プロパティのリスト  

<sup><sub>[*] 属性に型がない場合は、複数の型があるか、異なるフォーマット/パターンがある可能性があるためです</sub></sup>。  
- `anomalyType[string]`: 異常のクラスとグレード（クラス分けはメンテナンスによる。）  - `computedParameters[array]`: ListProperty。計算パラメータのリスト。  - `country[string]`: 予測に関連する国。  - `date[date]`: 予言の日付。  - `exceededThreshold[array]`: リストプロパティ。超過したしきい値のリスト。  - `head[string]`: 頭に関する情報。  - `interventionDuration[integer]`: 介入時間（分  - `laser[string]`: レーザー関連情報。  - `maintenanceTypeBin[string]`: メンテナンス・タイプのバイナリ表現。  - `maintenanceTypeDec[integer]`: メンテナンスタイプを10進数で表す。  - `requiresComponent[array]`: リストプロパティ。メンテナンスに必要な機械部品のリスト。  - `requiresSkill[array]`: ListProperty。必要な経験とツール  - `runningTime[integer]`: 上映時間（分）。  - `type[string]`: エンティティのタイプ（InventoryItem）。  - `weeksForIntervention[integer]`: 介入の期限（週単位）（anomalyClasが'Perfect'でこの値が52の場合、実際には介入は必要ない）。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
必須プロパティ  
- `anomalyType`  - `computedParameters`  - `date`  - `exceededThreshold`  - `head`  - `id`  - `interventionDuration`  - `laser`  - `maintenanceTypeBin`  - `maintenanceTypeDec`  - `requiresComponent`  - `requiresSkill`  - `runningTime`  - `type`  - `weeksForIntervention`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## プロパティのデータモデル記述  
アルファベット順（クリックで詳細表示）  
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
## ペイロードの例  
#### AIPrediction NGSI-v2 キー値の例  
JSON-LD形式のAIPredictionのkey-valuesの例です。これはNGSI-v2と互換性があり、`options=keyValues`を使うと個々のエンティティのコンテキストデータを返す。  
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
#### AIPrediction NGSI-v2 正規化例  
以下は、正規化されたJSON-LD形式のAIPredictionの例である。これは、オプションを使用しない場合、NGSI-v2と互換性があり、個々のエンティティのコンテキストデータを返します。  
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
#### AIPrediction NGSI-LD キー値の例  
AIPredictionのJSON-LD形式でのkey-valuesの例です。これはNGSI-LDと互換性があり、`options=keyValues`を使うと個々のエンティティのコンテキストデータを返す。  
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
#### AIPrediction NGSI-LD 正規化例  
以下は、正規化されたJSON-LD形式のAIPredictionの例である。これは、オプションを使用しない場合、NGSI-LDと互換性があり、個々のエンティティのコンテキストデータを返します。  
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
マグニチュード単位の扱い方については、[FAQ 10](https://smartdatamodels.org/index.php/faqs/)を参照のこと。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
