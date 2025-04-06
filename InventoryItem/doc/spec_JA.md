<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
エンティティInventoryItem  
===================<!-- /10-Header -->  
<!-- 15-License -->  
[オープン・ライセンス](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/InventoryItem/LICENSE.md)  
[文書が自動的に生成される](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
グローバルな説明**倉庫内の在庫を表す。  
バージョン: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## プロパティのリスト  

<sup><sub>[*] 属性に型がない場合は、複数の型があるか、異なるフォーマット/パターンがある可能性があるためです</sub></sup>。  
- `availableTotal[integer]`: アイテムの総利用可能数量。  - `itemLocation[string]`: アイテムの場所。  - `itemNumber[string]`: アイテムの一意の識別子。  - `name[string]`: アイテムの名前。  - `netWeight[number]`: 商品の正味重量。  - `onDelivery[integer]`: 商品の数量。  - `orderedBooked[integer]`: 注文され、予約された商品の数量。  - `physicalAvailability[integer]`: アイテムの物理的な入手可能性。  - `physicalBooked[integer]`: 商品の物理的な予約数量。  - `physicalStock[integer]`: 商品の物理的な在庫。  - `researchName[string]`: アイテムの研究名。  - `site[string]`: アイテムがあるサイト。  - `totalOrdered[integer]`: 商品の注文数量の合計。  - `type[string]`: エンティティのタイプ（InventoryItem）。  - `warehouseID[string]`: 倉庫の一意な識別子。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
必須プロパティ  
- `id`  - `itemNumber`  - `physicalStock`  - `type`  - `warehouseID`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## プロパティのデータモデル記述  
アルファベット順（クリックで詳細表示）  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
InventoryItem:    
  description: Represent an item of the inventory inside a warehouse    
  properties:    
    availableTotal:    
      description: The total available quantity of the item.    
      type: integer    
      x-ngsi:    
        type: Property    
    itemLocation:    
      description: The location of the item.    
      type: string    
      x-ngsi:    
        type: Property    
    itemNumber:    
      description: The unique identifier for the item.    
      type: string    
      x-ngsi:    
        type: Property    
    name:    
      description: The name of the item.    
      type: string    
      x-ngsi:    
        type: Property    
    netWeight:    
      description: The net weight of the item.    
      type: number    
      x-ngsi:    
        type: Property    
    onDelivery:    
      description: The quantity of the item on delivery.    
      type: integer    
      x-ngsi:    
        type: Property    
    orderedBooked:    
      description: The quantity of the item ordered and booked.    
      type: integer    
      x-ngsi:    
        type: Property    
    physicalAvailability:    
      description: The physical availability of the item.    
      type: integer    
      x-ngsi:    
        type: Property    
    physicalBooked:    
      description: The physical booked quantity of the item.    
      type: integer    
      x-ngsi:    
        type: Property    
    physicalStock:    
      description: The physical stock of the item.    
      type: integer    
      x-ngsi:    
        type: Property    
    researchName:    
      description: The research name of the item.    
      type: string    
      x-ngsi:    
        type: Property    
    site:    
      description: The site where the item is located.    
      type: string    
      x-ngsi:    
        type: Property    
    totalOrdered:    
      description: The total quantity ordered for the item.    
      type: integer    
      x-ngsi:    
        type: Property    
    type:    
      description: The type of the entity (InventoryItem).    
      type: string    
      x-ngsi:    
        type: Property    
    warehouseID:    
      description: The unique identifier for the warehouse.    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - warehouseID    
    - itemNumber    
    - physicalStock    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/InventoryItem/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/InventoryItem/schema.json    
  x-model-tags: maintenance    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## ペイロードの例  
#### InventoryItem NGSI-v2 キー値の例  
以下は、JSON-LD形式のInventoryItemをkey-valuesとした例である。これはNGSI-v2と互換性があり、`options=keyValues`を使用すると、個々のエンティティのコンテキストデータを返す。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/InventoryItem/inventoryItem01",  
    "type": "InventoryItem",  
    "warehouseID": "0000",  
    "itemNumber": "1055.52395.191",  
    "name": "Fusibile SIEMENS 3NA3 807",  
    "physicalStock": 10,  
    "researchName": "FusibileSIEMENS3NA38",  
    "site": "01",  
    "itemLocation": "SILO2/0027",  
    "netWeight": 0.13  
}  
```  
</details>  
#### InventoryItem NGSI-v2 正規化例  
以下は、正規化された JSON-LD 形式の InventoryItem の例である。これは、オプションを使用しない場合、NGSI-v2と互換性があり、個々のエンティティのコンテキストデータを返します。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:InventoryItem:inventoryItem01",  
    "type": "InventoryItem",  
    "warehouseID": {  
        "type": "Property",  
        "value": "0000"  
    },  
    "itemNumber": {  
        "type": "Property",  
        "value": "1055.52395.191"  
    },  
    "name": {  
        "type": "Property",  
        "value": "Fusibile SIEMENS 3NA3 807"  
    },  
    "physicalStock": {  
        "type": "Property",  
        "value": 10  
    },  
    "researchName": {  
        "type": "Property",  
        "value": "FusibileSIEMENS3NA38"  
    },  
    "site": {  
        "type": "Property",  
        "value": "01"  
    },  
    "itemLocation": {  
        "type": "Property",  
        "value": "SILO2/0027"  
    },  
    "netWeight": {  
        "type": "Property",  
        "value": 0.13  
    }  
}  
```  
</details>  
#### InventoryItem NGSI-LD キー値の例  
以下は、JSON-LD形式のInventoryItemをkey-valuesとした例である。これは NGSI-LD と互換性があり、`options=keyValues` を使用すると個々のエンティティのコンテキストデータを返す。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/InventoryItem/inventoryItem01",  
    "type": "InventoryItem",  
    "warehouseID": "0000",  
    "itemNumber": "1055.52395.191",  
    "name": "Fusibile SIEMENS 3NA3 807",  
    "physicalStock": 10,  
    "researchName": "FusibileSIEMENS3NA38",  
    "site": "01",  
    "itemLocation": "SILO2/0027",  
    "netWeight": 0.13  
}  
```  
</details>  
#### InventoryItem NGSI-LD 正規化例  
以下は、正規化された JSON-LD 形式の InventoryItem の例である。これは、オプションを使用しない場合はNGSI-LDと互換性があり、個々のエンティティのコンテキストデータを返します。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/InventoryItem/inventoryItem01",  
    "type": "InventoryItem",  
    "warehouseID": {  
        "type": "Property",  
        "value": "0000"  
    },  
    "itemNumber": {  
        "type": "Property",  
        "value": "1055.52395.191"  
    },  
    "name": {  
        "type": "Property",  
        "value": "Fusibile SIEMENS 3NA3 807"  
    },  
    "physicalStock": {  
        "type": "Property",  
        "value": 10  
    },  
    "researchName": {  
        "type": "Property",  
        "value": "FusibileSIEMENS3NA38"  
    },  
    "site": {  
        "type": "Property",  
        "value": "01"  
    },  
    "itemLocation": {  
        "type": "Property",  
        "value": "SILO2/0027"  
    },  
    "netWeight": {  
        "type": "Property",  
        "value": 0.13  
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
