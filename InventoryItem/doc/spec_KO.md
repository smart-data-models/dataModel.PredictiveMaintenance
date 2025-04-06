<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
엔티티: 인벤토리 항목  
============<!-- /10-Header -->  
<!-- 15-License -->  
[오픈 라이선스](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/InventoryItem/LICENSE.md)  
[문서 자동 생성](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
글로벌 설명: **창고 내부의 인벤토리 항목을 나타냅니다**.  
버전: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 속성 목록  

<sup><sub>[*] 속성에 유형이 없는 것은 여러 유형 또는 다른 형식/패턴을 가질 수 있기 때문입니다</sub></sup>.  
- `availableTotal[integer]`: 아이템의 총 사용 가능한 수량입니다.  - `itemLocation[string]`: 항목의 위치입니다.  - `itemNumber[string]`: 항목의 고유 식별자입니다.  - `name[string]`: 항목의 이름입니다.  - `netWeight[number]`: 아이템의 순중량입니다.  - `onDelivery[integer]`: 배송 중인 품목의 수량입니다.  - `orderedBooked[integer]`: 주문 및 예약한 품목의 수량입니다.  - `physicalAvailability[integer]`: 아이템의 실제 사용 가능 여부입니다.  - `physicalBooked[integer]`: 품목의 실제 예약 수량입니다.  - `physicalStock[integer]`: 아이템의 실제 재고입니다.  - `researchName[string]`: 항목의 연구 이름입니다.  - `site[string]`: 항목이 위치한 사이트입니다.  - `totalOrdered[integer]`: 품목에 대해 주문한 총 수량입니다.  - `type[string]`: 엔티티의 유형(인벤토리 항목)입니다.  - `warehouseID[string]`: 창고에 대한 고유 식별자입니다.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
필수 속성  
- `id`  - `itemNumber`  - `physicalStock`  - `type`  - `warehouseID`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 속성에 대한 데이터 모델 설명  
알파벳순으로 정렬(자세한 내용을 보려면 클릭)  
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
## 페이로드 예시  
#### 인벤토리 항목 NGSI-v2 키 값 예제  
다음은 JSON-LD 형식의 인벤토리 항목을 키값으로 사용하는 예시입니다. 이는 `옵션=키값`을 사용할 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 인벤토리 항목 NGSI-v2 정규화 예제  
다음은 정규화된 JSON-LD 형식의 InventoryItem 예시입니다. 이는 옵션을 사용하지 않을 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 인벤토리 항목 NGSI-LD 키 값 예제  
다음은 JSON-LD 형식의 인벤토리 항목을 키값으로 사용하는 예시입니다. 이는 `옵션=키값`을 사용할 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 인벤토리 항목 NGSI-LD 정규화 예제  
다음은 정규화된 JSON-LD 형식의 InventoryItem 예시입니다. 이는 옵션을 사용하지 않을 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
규모 단위를 다루는 방법에 대한 답변은 [FAQ 10](https://smartdatamodels.org/index.php/faqs/)을 참조하세요.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
