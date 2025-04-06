<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
엔티티: 머신 컴포넌트  
============<!-- /10-Header -->  
<!-- 15-License -->  
[오픈 라이선스](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MachineComponent/LICENSE.md)  
[문서 자동 생성](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
글로벌 설명: **기계 내부에 있거나 교체할 구성 요소를 나타냅니다**.  
버전: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 속성 목록  

<sup><sub>[*] 속성에 유형이 없는 것은 여러 유형 또는 다른 형식/패턴을 가질 수 있기 때문입니다</sub></sup>.  
- `componentCost[number]`: 유로 단위의 고객 비용입니다.  - `componentDescription[string]`: 제품 이름과 간단한 설명, 공급업체 사이트로 연결되는 링크도 제공합니다.  - `componentSupplierID[string]`: 공급업체 구성 요소 코드 - 원본.  - `dateGuaranteedDelivery[date]`: 공급업체에서 보장된 사용 가능 날짜를 확인했습니다.  - `deliveryCost[number]`: 유로 단위의 고객 비용입니다.  - `locationInWarehouse[string]`: 컴포넌트 위치를 식별합니다.  - `measurement[object]`: 컴포넌트의 물리적 속성  	- `height[object]`: 개체의 높이 측정.    
	- `length[object]`: 객체의 길이입니다.    
	- `weight[object]`: 물체의 무게를 측정합니다.    
	- `width[object]`: 개체의 너비를 측정합니다.    
- `numberOfPiecesAvailable[integer]`: 여러 물류창고의 현재 재고 현황을 확인할 수 있습니다.  - `numberOfPiecesOnDelivery[integer]`: 주문 진행 중 - 주문 확인에 대한 정보입니다.  - `requiresSkill[array]`: ListProperty. 경험과 도구가 필요합니다.  - `supplierID[string]`: 공급업체 식별 - 연락처 및 정보  - `type[string]`: 엔티티의 유형(머신 컴포넌트)입니다.  - `warehouseID[string]`: 서비스 공급업체의 고객과 함께 창고 위치를 파악합니다.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
필수 속성  
- `componentDescription`  - `componentSupplierID`  - `id`  - `locationInWarehouse`  - `measurement`  - `requiresSkill`  - `supplierID`  - `type`  - `warehouseID`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 속성에 대한 데이터 모델 설명  
알파벳순으로 정렬(자세한 내용을 보려면 클릭)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
MachineComponent:    
  description: Represent a component inside a machine or to be replaced    
  properties:    
    componentCost:    
      description: Cost for the customer in Euros.    
      type: number    
      x-ngsi:    
        type: Property    
    componentDescription:    
      description: Product Name and a brief description, also link to supplier site.    
      type: string    
      x-ngsi:    
        type: Property    
    componentSupplierID:    
      description: Supplier Component Code - Original.    
      type: string    
      x-ngsi:    
        type: Property    
    dateGuaranteedDelivery:    
      description: Guaranteed availability date confirmed by supplier.    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    deliveryCost:    
      description: Cost for the customer in Euros.    
      type: number    
      x-ngsi:    
        type: Property    
    locationInWarehouse:    
      description: Identify the component location.    
      type: string    
      x-ngsi:    
        type: Property    
    measurement:    
      description: The physical properties of the component    
      properties:    
        height:    
          description: Height measurement of the object.    
          properties:    
            unit:    
              default: cm    
              description: Unit of measurement for height (e.g., cm, m, in).    
              type: string    
              x-ngsi:    
                type: Property    
            value:    
              description: Height value of the object.    
              type: number    
              x-ngsi:    
                type: Property    
          required:    
            - value    
            - unit    
          type: object    
          x-ngsi:    
            type: Property    
        length:    
          description: Length of the object.    
          properties:    
            unit:    
              default: cm    
              description: Unit of measurement for length (e.g., cm, m, in).    
              type: string    
              x-ngsi:    
                type: Property    
            value:    
              description: Length value of the object.    
              type: number    
              x-ngsi:    
                type: Property    
          required:    
            - value    
            - unit    
          type: object    
          x-ngsi:    
            type: Property    
        weight:    
          description: Weight measurement of the object.    
          properties:    
            unit:    
              default: kg    
              description: Unit of measurement for weight (e.g., kg, lb).    
              type: string    
              x-ngsi:    
                type: Property    
            value:    
              description: Weight value of the object.    
              type: number    
              x-ngsi:    
                type: Property    
          required:    
            - value    
            - unit    
          type: object    
          x-ngsi:    
            type: Property    
        width:    
          description: Width measurement of the object.    
          properties:    
            unit:    
              default: cm    
              description: Unit of measurement for width (e.g., cm, m, in).    
              type: string    
              x-ngsi:    
                type: Property    
            value:    
              description: Width value of the object.    
              type: number    
              x-ngsi:    
                type: Property    
          required:    
            - value    
            - unit    
          type: object    
          x-ngsi:    
            type: Property    
      required:    
        - height    
        - width    
        - length    
        - weight    
      type: object    
      x-ngsi:    
        type: Property    
    numberOfPiecesAvailable:    
      description: Current stock availability in different warehouses.    
      type: integer    
      x-ngsi:    
        type: Property    
    numberOfPiecesOnDelivery:    
      description: Order in progress - Info about order confirmation.    
      type: integer    
      x-ngsi:    
        type: Property    
    requiresSkill:    
      description: ListProperty. Experience and tools required.    
      items:    
        description: Technical skill description.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    supplierID:    
      description: Identify the Supplier - Contact and info.    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: The type of the entity (MachineComponent).    
      type: string    
      x-ngsi:    
        type: Property    
    warehouseID:    
      description: Identify the warehouse places, also c/o customer of service suppliers.    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - componentSupplierID    
    - componentDescription    
    - requiresSkill    
    - supplierID    
    - warehouseID    
    - locationInWarehouse    
    - measurement    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/MachineComponent/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MachineComponent/schema.json    
  x-model-tags: maintenance    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## 페이로드 예시  
#### 머신 컴포넌트 NGSI-v2 키 값 예제  
다음은 키 값으로 JSON-LD 형식의 MachineComponent의 예입니다. 이는 `옵션=키값`을 사용할 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceComponent/maintenanceComponent01",  
    "type": "MaintenanceComponent",  
    "componentSupplierID": "SUP12345",  
    "componentDescription": "High-Performance Motor with advanced features and link to supplier site.",  
    "requiresSkill": [  
        "MaintenanceSkill:maintenanceSkill01"  
    ],  
    "supplierID": "SUP001",  
    "warehouseID": "WH001",  
    "locationInWarehouse": "Aisle 5, Shelf 3",  
    "numberOfPiecesAvailable": 50,  
    "numberOfPiecesOnDelivery": 20,  
    "dateGuaranteedDelivery": "2023-12-31",  
    "measurement": {  
        "height": {  
            "value": 10.5,  
            "unit": "cm"  
        },  
        "width": {  
            "value": 15.2,  
            "unit": "cm"  
        },  
        "length": {  
            "value": 20.8,  
            "unit": "cm"  
        },  
        "weight": {  
            "value": 5.5,  
            "unit": "kg"  
        }  
    },  
    "componentCost": 250.75,  
    "deliveryCost": 15.50  
}  
```  
</details>  
#### 머신 컴포넌트 NGSI-v2 정규화 예제  
다음은 정규화된 JSON-LD 형식의 머신 컴포넌트 예시입니다. 이는 옵션을 사용하지 않을 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:MachineComponent:machineComponent01",  
    "type": "MachineComponent",  
    "componentSupplierID": {  
        "type": "Property",  
        "value": "SUP12345"  
    },  
    "componentDescription": {  
        "type": "Property",  
        "value": "High-Performance Motor with advanced features and link to supplier site."  
    },  
    "requiresSkill": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Property",  
                "id": "MaintenanceSkill:maintenanceSkill01"  
            }  
        ]  
    },  
    "supplierID": {  
        "type": "Property",  
        "value": "SUP001"  
    },  
    "warehouseID": {  
        "type": "Property",  
        "value": "WH001"  
    },  
    "locationInWarehouse": {  
        "type": "Property",  
        "value": "Aisle 5, Shelf 3"  
    },  
    "numberOfPiecesAvailable": {  
        "type": "Integer",  
        "value": 50  
    },  
    "numberOfPiecesOnDelivery": {  
        "type": "Integer",  
        "value": 20  
    },  
    "dateGuaranteedDelivery": {  
        "type": "Property",  
        "value": "2023-12-31"  
    },  
    "measurement": {  
        "type": "Property",  
        "value": {  
            "height": {  
                "value": {  
                    "type": "Property",  
                    "value": 10.5  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "width": {  
                "value": {  
                    "type": "Property",  
                    "value": 15.2  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "length": {  
                "value": {  
                    "type": "Property",  
                    "value": 20.8  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "weight": {  
                "value": {  
                    "type": "Property",  
                    "value": 5.5  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "kg"  
                }  
            }  
        }  
    },  
    "componentCost": {  
        "type": "Property",  
        "value": 250.75  
    },  
    "deliveryCost": {  
        "type": "Property",  
        "value": 15.50  
    }  
}  
```  
</details>  
#### 머신 컴포넌트 NGSI-LD 키 값 예제  
다음은 키 값으로 JSON-LD 형식의 MachineComponent의 예입니다. 이는 `옵션=키값`을 사용할 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MachineComponent/machineComponent01",  
    "type": "MachineComponent",  
    "componentSupplierID": "SUP12345",  
    "componentDescription": "High-Performance Motor with advanced features and link to supplier site.",  
    "requiresSkill": [  
        "MaintenanceSkill:maintenanceSkill01"  
    ],  
    "supplierID": "SUP001",  
    "warehouseID": "WH001",  
    "locationInWarehouse": "Aisle 5, Shelf 3",  
    "numberOfPiecesAvailable": 50,  
    "numberOfPiecesOnDelivery": 20,  
    "dateGuaranteedDelivery": "2023-12-31",  
    "measurement": {  
        "height": {  
            "value": 10.5,  
            "unit": "cm"  
        },  
        "width": {  
            "value": 15.2,  
            "unit": "cm"  
        },  
        "length": {  
            "value": 20.8,  
            "unit": "cm"  
        },  
        "weight": {  
            "value": 5.5,  
            "unit": "kg"  
        }  
    },  
    "componentCost": 250.75,  
    "deliveryCost": 15.50  
}  
```  
</details>  
#### 머신 컴포넌트 NGSI-LD 정규화 예제  
다음은 정규화된 JSON-LD 형식의 머신 컴포넌트 예시입니다. 이는 옵션을 사용하지 않을 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MachineComponent/machineComponent01",  
    "type": "MachineComponent",  
    "componentSupplierID": {  
        "type": "Property",  
        "value": "SUP12345"  
    },  
    "componentDescription": {  
        "type": "Property",  
        "value": "High-Performance Motor with advanced features and link to supplier site."  
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
    "supplierID": {  
        "type": "Property",  
        "value": "SUP001"  
    },  
    "warehouseID": {  
        "type": "Property",  
        "value": "WH001"  
    },  
    "locationInWarehouse": {  
        "type": "Property",  
        "value": "Aisle 5, Shelf 3"  
    },  
    "numberOfPiecesAvailable": {  
        "type": "Property",  
        "value": 50  
    },  
    "numberOfPiecesOnDelivery": {  
        "type": "Property",  
        "value": 20  
    },  
    "dateGuaranteedDelivery": {  
        "type": "Property",  
        "value": "2023-12-31"  
    },  
    "measurement": {  
        "type": "Property",  
        "value": {  
            "height": {  
                "value": {  
                    "type": "Property",  
                    "value": 10.5  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "width": {  
                "value": {  
                    "type": "Property",  
                    "value": 15.2  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "length": {  
                "value": {  
                    "type": "Property",  
                    "value": 20.8  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "weight": {  
                "value": {  
                    "type": "Property",  
                    "value": 5.5  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "kg"  
                }  
            }  
        }  
    },  
    "componentCost": {  
        "type": "Property",  
        "value": 250.75  
    },  
    "deliveryCost": {  
        "type": "Property",  
        "value": 15.50  
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
