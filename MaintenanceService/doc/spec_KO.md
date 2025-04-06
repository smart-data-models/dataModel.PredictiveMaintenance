<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
엔티티: 유지보수 서비스  
=============<!-- /10-Header -->  
<!-- 15-License -->  
[오픈 라이선스](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MaintenanceService/LICENSE.md)  
[문서 자동 생성](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
글로벌 설명: **예정된 유지보수 작업을 나타냅니다**.  
버전: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 속성 목록  

<sup><sub>[*] 속성에 유형이 없는 것은 여러 유형 또는 다른 형식/패턴을 가질 수 있기 때문입니다</sub></sup>.  
- `activityRequiredOfCustomer[array]`: ListProperty. 유지 관리를 위한 고객 준비 활동(고객이 확인해야 함).  - `anomalyIndicator[array]`: ListProperty. 이상 징후에 대한 기술 정보(분석에 대한 정보)입니다.  - `anomalyType[string]`: 이상 상태의 분류 및 등급(유지보수를 참조한 분류).  - `costForecast[number]`: 활동의 계산된 비용(유지 관리가 끝나면 확인 예정).  - `customerID[string]`: 고객을 식별합니다.  - `durationOfOperation[number]`: 시스템에서의 작업 시간(활동을 실행하는 데 걸리는 시간).  - `hasConfiguration[array]`: ListProperty. 머신 설명입니다.  - `machineAddressLocation[string]`: 기기 주소(공장 주소).  - `machineID[string]`: 시스템을 식별합니다(S/N 또는 고유 식별자).  - `maintenanceDateScheduled[date]`: 제안된 유지 관리 날짜(고객이 확인 예정).  - `maintenanceDeadline[date]`: (최적의 조치를 위한 마지막 날짜)까지 유지 관리가 필요합니다.  - `maintenanceOperator[uri]`: 활동을 담당하는 운영자.  - `maintenanceRequired[array]`: ListProperty. 유지 관리 서비스 설명(활동 목록).  - `requiresComponent[array]`: ListProperty. 유지보수에 필요한 기계 구성 요소 목록입니다.  - `type[string]`: 엔티티의 유형(유지보수 서비스)입니다.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
필수 속성  
- `activityRequiredOfCustomer`  - `anomalyIndicator`  - `anomalyType`  - `costForecast`  - `customerID`  - `durationOfOperation`  - `hasConfiguration`  - `id`  - `machineAddressLocation`  - `machineID`  - `maintenanceDateScheduled`  - `maintenanceDeadline`  - `maintenanceOperator`  - `maintenanceRequired`  - `requiresComponent`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 속성에 대한 데이터 모델 설명  
알파벳순으로 정렬(자세한 내용을 보려면 클릭)  
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
## 페이로드 예시  
#### 유지보수 서비스 NGSI-v2 키 값 예제  
다음은 키 값으로 JSON-LD 형식의 유지보수 서비스 예제입니다. 이는 `옵션=키값`을 사용할 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 유지보수 서비스 NGSI-v2 정규화 예제  
다음은 정규화된 JSON-LD 형식의 유지보수 서비스 예시입니다. 이는 옵션을 사용하지 않을 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 유지보수 서비스 NGSI-LD 키 값 예제  
다음은 키 값으로 JSON-LD 형식의 유지보수 서비스의 예입니다. 이는 `옵션=키값`을 사용할 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 유지보수 서비스 NGSI-LD 정규화 예제  
다음은 정규화된 JSON-LD 형식의 유지보수 서비스의 예입니다. 이는 옵션을 사용하지 않을 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
규모 단위를 다루는 방법에 대한 답변은 [FAQ 10](https://smartdatamodels.org/index.php/faqs/)을 참조하세요.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
