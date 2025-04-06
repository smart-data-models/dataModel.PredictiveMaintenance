<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
エンティティメンテナンスサービス  
================<!-- /10-Header -->  
<!-- 15-License -->  
[オープン・ライセンス](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MaintenanceService/LICENSE.md)  
[文書が自動的に生成される](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
グローバルな説明**定期メンテナンスの実施**。  
バージョン: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## プロパティのリスト  

<sup><sub>[*] 属性に型がない場合は、複数の型があるか、異なるフォーマット/パターンがある可能性があるためです</sub></sup>。  
- `activityRequiredOfCustomer[array]`: リストプロパティメンテナンスのためのお客様準備活動（お客様にご確認いただきます。）  - `anomalyIndicator[array]`: リストプロパティ異常に関する技術情報（分析情報）。  - `anomalyType[string]`: 異常のクラスとグレード（クラス分けはメンテナンスによる。）  - `costForecast[number]`: 活動費用の算出（メンテナンス終了時に確認）。  - `customerID[string]`: 顧客を特定する。  - `durationOfOperation[number]`: システムの作業時間（アクティビティの実行時間数）。  - `hasConfiguration[array]`: リストプロパティ。マシンの説明  - `machineAddressLocation[string]`: マシンアドレス（工場アドレス）。  - `machineID[string]`: システムを識別する（S/Nまたは固有識別子）。  - `maintenanceDateScheduled[date]`: メンテナンス日（お客様にご確認いただきます。）  - `maintenanceDeadline[date]`: メンテナンスの必要期限 ... (最適な処置の最終期限)。  - `maintenanceOperator[uri]`: アクティビティを担当するオペレーター。  - `maintenanceRequired[array]`: リストプロパティ。保守サービスの説明（アクティビティのリスト）。  - `requiresComponent[array]`: リストプロパティ。メンテナンスに必要な機械部品のリスト。  - `type[string]`: エンティティのタイプ（MaintenanceService）。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
必須プロパティ  
- `activityRequiredOfCustomer`  - `anomalyIndicator`  - `anomalyType`  - `costForecast`  - `customerID`  - `durationOfOperation`  - `hasConfiguration`  - `id`  - `machineAddressLocation`  - `machineID`  - `maintenanceDateScheduled`  - `maintenanceDeadline`  - `maintenanceOperator`  - `maintenanceRequired`  - `requiresComponent`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## プロパティのデータモデル記述  
アルファベット順（クリックで詳細表示）  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
MaintenanceService:    
  description: Represent a scheduled maintenance operation    
  properties:    
    activityRequiredOfCustomer:    
      description: ListProperty. Customer preparation activities for maintenance (To be confirmed by customer).    
      items:    
        description: Required activities.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    anomalyIndicator:    
      description: ListProperty. Technical information about the anomaly (Information on analysis).    
      items:    
        description: Technical information about the anomaly (Information on analysis).    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    anomalyType:    
      description: Class and Grade of anomaly (Classification referred to the maintenance).    
      type: string    
      x-ngsi:    
        type: Property    
    costForecast:    
      description: Calculated cost of the activity (To be confirmed at the end of maintenance).    
      type: number    
      x-ngsi:    
        type: Property    
    customerID:    
      description: Identify the customer.    
      type: string    
      x-ngsi:    
        type: Property    
    durationOfOperation:    
      description: Working time on system (Number of hours to execute the activity).    
      type: number    
      x-ngsi:    
        type: Property    
    hasConfiguration:    
      description: ListProperty. Machine description.    
      items:    
        description: List of components & options.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    machineAddressLocation:    
      description: Machine address (Factory address).    
      type: string    
      x-ngsi:    
        type: Property    
    machineID:    
      description: Identify the system (S/N or Unique Identifier).    
      type: string    
      x-ngsi:    
        type: Property    
    maintenanceDateScheduled:    
      description: Maintenance date proposed (To be confirmed by customer).    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    maintenanceDeadline:    
      description: Maintenance required by .. (Last date for optimal action).    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    maintenanceOperator:    
      description: Operator in charge of the activity.    
      format: uri    
      type: string    
      x-ngsi:    
        type: Relationship    
    maintenanceRequired:    
      description: ListProperty. Maintenance Service description (List of activity).    
      items:    
        description: Required maintenance activity.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    requiresComponent:    
      description: ListProperty. List of machine components required for the maintenance.    
      items:    
        description: Required machine components.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    type:    
      description: The type of the entity (MaintenanceService).    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - machineID    
    - customerID    
    - machineAddressLocation    
    - hasConfiguration    
    - anomalyType    
    - anomalyIndicator    
    - maintenanceDeadline    
    - maintenanceDateScheduled    
    - maintenanceRequired    
    - maintenanceOperator    
    - requiresComponent    
    - durationOfOperation    
    - activityRequiredOfCustomer    
    - costForecast    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/MaintenanceService/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceService/schema.json    
  x-model-tags: maintenace    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## ペイロードの例  
#### MaintenanceService NGSI-v2 キー値の例  
JSON-LD形式のMaintenanceServiceのkey-valuesの例である。これはNGSI-v2と互換性があり、`options=keyValues`を使用すると個々のエンティティのコンテキストデータを返す。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceService/maintenanceService01",  
    "type": "MaintenanceService",  
    "machineID": "S/N123456789",  
    "customerID": "CUST001",  
    "machineAddressLocation": "123 Factory Street, Anytown, USA",  
    "hasConfiguration": [  
        "MachineComponent:machineComponent01"  
    ],  
    "anomalyType": "ClassA-Grade1",  
    "anomalyIndicator": [  
        "High Temperature",  
        "Unusual Vibration"  
    ],  
    "maintenanceDeadline": "2023-10-20",  
    "maintenanceDateScheduled": "2023-10-19",  
    "maintenanceRequired": [  
        "Replace ComponentA",  
        "Lubricate ComponentB"  
    ],  
    "maintenanceOperator": "ServiceTechnician:serviceTechnician01",  
    "requiresComponent": [  
        "MachineComponent:machineComponent01"  
    ],  
    "durationOfOperation": 4.5,  
    "activityRequiredOfCustomer": [  
        "Clear workstation",  
        "Dispose of WIPs"  
    ],  
    "costForecast": 1000  
}  
```  
</details>  
#### メンテナンスサービス NGSI-v2 正規化例  
以下は、正規化された JSON-LD 形式の MaintenanceService の例である。これは、オプションを使用しない場合、NGSI-v2と互換性があり、個々のエンティティのコンテキストデータを返します。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:MaintenanceService:maintenanceService01",  
    "type": "MaintenanceService",  
    "machineID": {  
        "type": "Property",  
        "value": "S/N123456789"  
    },  
    "customerID": {  
        "type": "Property",  
        "value": "CUST001"  
    },  
    "machineAddressLocation": {  
        "type": "Property",  
        "value": "123 Factory Street, Anytown, USA"  
    },  
    "hasConfiguration": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MachineComponent:machineComponent01"  
            }  
        ]  
    },  
    "anomalyType": {  
        "type": "Property",  
        "value": "ClassA-Grade1"  
    },  
    "anomalyIndicator": {  
        "type": "Property",  
        "value": [  
            "High Temperature",  
            "Unusual Vibration"  
        ]  
    },  
    "maintenanceDeadline": {  
        "type": "Property",  
        "value": "2023-10-20"  
    },  
    "maintenanceDateScheduled": {  
        "type": "Property",  
        "value": "2023-10-19"  
    },  
    "maintenanceRequired": {  
        "type": "ListProperty",  
        "value": [  
            "Replace ComponentA",  
            "Lubricate ComponentB"  
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
    "durationOfOperation": {  
        "type": "Number",  
        "value": 4.5  
    },  
    "activityRequiredOfCustomer": {  
        "type": "ListProperty",  
        "value": [  
            "Clear workstation",  
            "Dispose of WIPs"  
        ]  
    },  
    "costForecast": {  
        "type": "number",  
        "value": 1000  
    }  
}  
```  
</details>  
#### 保守サービス NGSI-LD キー値の例  
JSON-LD形式のMaintenanceServiceのkey-valuesの例です。これは NGSI-LD と互換性があり、`options=keyValues` を使うと個々のエンティティのコンテキストデータを返す。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceService/maintenanceService01",  
    "type": "MaintenanceService",  
    "machineID": "S/N123456789",  
    "customerID": "CUST001",  
    "machineAddressLocation": "123 Factory Street, Anytown, USA",  
    "hasConfiguration": [  
        "MachineComponent:machineComponent01"  
    ],  
    "anomalyType": "ClassA-Grade1",  
    "anomalyIndicator": [  
        "High Temperature",  
        "Unusual Vibration"  
    ],  
    "maintenanceDeadline": "2023-10-20",  
    "maintenanceDateScheduled": "2023-10-19",  
    "maintenanceRequired": [  
        "Replace ComponentA",  
        "Lubricate ComponentB"  
    ],  
    "maintenanceOperator": "ServiceTechnician:serviceTechnician01",  
    "requiresComponent": [  
        "MachineComponent:machineComponent01"  
    ],  
    "durationOfOperation": 4.5,  
    "activityRequiredOfCustomer": [  
        "Clear workstation",  
        "Dispose of WIPs"  
    ],  
    "costForecast": 1000  
}  
```  
</details>  
#### メンテナンスサービス NGSI-LD 正規化例  
以下は、正規化されたJSON-LD形式のMaintenanceServiceの例である。これは、オプションを使用しない場合はNGSI-LDと互換性があり、個々のエンティティのコンテキストデータを返します。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceService/maintenanceService01",  
    "type": "MaintenanceService",  
    "machineID": {  
        "type": "Property",  
        "value": "S/N123456789"  
    },  
    "customerID": {  
        "type": "Property",  
        "value": "CUST001"  
    },  
    "machineAddressLocation": {  
        "type": "Property",  
        "value": "123 Factory Street, Anytown, USA"  
    },  
    "hasConfiguration": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MachineComponent:machineComponent01"  
            }  
        ]  
    },  
    "anomalyType": {  
        "type": "Property",  
        "value": "ClassA-Grade1"  
    },  
    "anomalyIndicator": {  
        "type": "ListProperty",  
        "value": [  
            "High Temperature",  
            "Unusual Vibration"  
        ]  
    },  
    "maintenanceDeadline": {  
        "type": "Property",  
        "value": "2023-10-20"  
    },  
    "maintenanceDateScheduled": {  
        "type": "Property",  
        "value": "2023-10-19"  
    },  
    "maintenanceRequired": {  
        "type": "ListProperty",  
        "value": [  
            "Replace ComponentA",  
            "Lubricate ComponentB"  
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
    "durationOfOperation": {  
        "type": "Property",  
        "value": 4.5  
    },  
    "activityRequiredOfCustomer": {  
        "type": "Property",  
        "value": [  
            "Clear workstation",  
            "Dispose of WIPs"  
        ]  
    },  
    "costForecast": {  
        "type": "Property",  
        "value": 1000  
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
