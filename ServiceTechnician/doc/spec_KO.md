<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entity: 서비스 기술자  
===============<!-- /10-Header -->  
<!-- 15-License -->  
[오픈 라이선스](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/ServiceTechnician/LICENSE.md)  
[문서 자동 생성](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
글로벌 설명: **서비스를 제공하는 유지보수 운영자를 나타냅니다**.  
버전: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 속성 목록  

<sup><sub>[*] 속성에 유형이 없는 것은 여러 유형 또는 다른 형식/패턴을 가질 수 있기 때문입니다</sub></sup>.  
- `calendar[array]`: 목록 속성. 계획된 활동 목록입니다.  - `geographicalArea[string]`: 지역 및 위치의 정의.  - `hasSkill[array]`: ListProperty. 기능 및 경험에 대한 설명입니다.  - `historicalService[array]`: ListProperty. 관리되는 서비스 목록입니다.  - `organization[string]`: 기술자가 소속된 조직(PRIMA 지사 또는 외부 사무실).  - `referenceAddress[string]`: 시작 위치(사무실 및 집).  - `toolProvided[array]`: 목록 속성. 기술 장비(모든 팀에 특수 장비가 항상 제공되는 것은 아님).  - `type[string]`: 엔티티의 유형(서비스 기술자)입니다.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
필수 속성  
- `calendar`  - `geographicalArea`  - `hasSkill`  - `historicalService`  - `id`  - `organization`  - `referenceAddress`  - `toolProvided`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 속성에 대한 데이터 모델 설명  
알파벳순으로 정렬(자세한 내용을 보려면 클릭)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
ServiceTechnician:    
  description: Represent a maintenance operator providing the service    
  properties:    
    calendar:    
      description: ListProperty. List of planned activities.    
      items:    
        description: Calendar of activities for the period already planned.    
        format: date    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    geographicalArea:    
      description: Definition of the area and location.    
      type: string    
      x-ngsi:    
        type: Property    
    hasSkill:    
      description: ListProperty. Description of capabilities and experiences.    
      items:    
        description: Description of capabilities and experiences.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    historicalService:    
      description: ListProperty. List of managed services.    
      items:    
        description: Managed service.    
        format: date    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    organization:    
      description: Organization to which the technician belongs (PRIMA branch or external office).    
      type: string    
      x-ngsi:    
        type: Property    
    referenceAddress:    
      description: Starting position (Office and Home).    
      type: string    
      x-ngsi:    
        type: Property    
    toolProvided:    
      description: ListProperty. Technical equipment (special equipment not always provided for all teams).    
      items:    
        description: Name of the required tool.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    type:    
      description: The type of the entity (ServiceTechnician).    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - organization    
    - hasSkill    
    - toolProvided    
    - geographicalArea    
    - referenceAddress    
    - calendar    
    - historicalService    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/ServiceTechnician/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/ServiceTechnician/schema.json    
  x-model-tags: maintenace    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## 페이로드 예시  
#### ServiceTechnician NGSI-v2 키 값 예제  
다음은 키 값으로 JSON-LD 형식의 서비스 기술자의 예입니다. 이는 `옵션=키값`을 사용할 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/ServiceTechnician/serviceTechnician01",  
    "type": "ServiceTechnician",  
    "organization": "PRIMA Branch A",  
    "hasSkill": [  
        "MaintenanceSkill:maintenanceSkillID"  
    ],  
    "toolProvided": [  
        "Multimeter",  
        "Screwdriver Set",  
        "Pliers Set"  
    ],  
    "geographicalArea": "North Region",  
    "referenceAddress": "123 Main Street, Anytown, USA",  
    "calendar": [  
        "2023-10-01",  
        "2023-10-05",  
        "2023-10-10"  
    ],  
    "historicalService": [  
        "2023-09-15",  
        "2023-09-20",  
        "2023-09-25"  
    ]  
}  
```  
</details>  
#### ServiceTechnician NGSI-v2 정규화 예제  
다음은 정규화된 JSON-LD 형식의 서비스 기술자의 예입니다. 이는 옵션을 사용하지 않을 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:ServiceTechnician:serviceTechnician01",  
    "type": "ServiceTechnician",  
    "organization": {  
        "type": "Text",  
        "value": "PRIMA Branch A"  
    },  
    "hasSkill": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MaintenanceSkill:maintenanceSkill01"  
            }  
        ]  
    },  
    "toolProvided": {  
        "type": "Text",  
        "value": [  
            "Multimeter",  
            "Screwdriver Set",  
            "Pliers Set"  
        ]  
    },  
    "geographicalArea": {  
        "type": "Text",  
        "value": "North Region"  
    },  
    "referenceAddress": {  
        "type": "Text",  
        "value": "123 Main Street, Anytown, USA"  
    },  
    "calendar": {  
        "type": "Date",  
        "value": [  
            "2023-10-01",  
            "2023-10-05",  
            "2023-10-10"  
        ]  
    },  
    "historicalService": {  
        "type": "Date",  
        "value": [  
            "2023-09-15",  
            "2023-09-20",  
            "2023-09-25"  
        ]  
    }  
}  
```  
</details>  
#### ServiceTechnician NGSI-LD 키 값 예시  
다음은 키 값으로 JSON-LD 형식의 서비스 기술자의 예입니다. 이는 `옵션=키값`을 사용할 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "type": "ServiceTechnician",  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/ServiceTechnician/serviceTechnician01",  
    "organization": "PRIMA Branch A",  
    "hasSkill": [  
        "MaintenanceSkill:maintenanceSkillID"  
    ],  
    "toolProvided": [  
        "Multimeter",  
        "Screwdriver Set",  
        "Pliers Set"  
    ],  
    "geographicalArea": "North Region",  
    "referenceAddress": "123 Main Street, Anytown, USA",  
    "calendar": [  
        "2023-10-01",  
        "2023-10-05",  
        "2023-10-10"  
    ],  
    "historicalService": [  
        "2023-09-15",  
        "2023-09-20",  
        "2023-09-25"  
    ]  
}  
```  
</details>  
#### ServiceTechnician NGSI-LD 정규화 예제  
다음은 정규화된 JSON-LD 형식의 ServiceTechnician 예제입니다. 이는 옵션을 사용하지 않을 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/ServiceTechnician/serviceTechnician01",  
    "type": "ServiceTechnician",  
    "organization": {  
        "type": "Property",  
        "value": "PRIMA Branch A"  
    },  
    "hasSkill": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "object": "urn:ngsi-ld:dataModel.PredictiveMaintenance:MaintenanceSkill:maintenanceSkill01"  
            }  
        ]  
    },  
    "toolProvided": {  
        "type": "ListProperty",  
        "value": [  
            "Multimeter",  
            "Screwdriver Set",  
            "Pliers Set"  
        ]  
    },  
    "geographicalArea": {  
        "type": "Property",  
        "value": "North Region"  
    },  
    "referenceAddress": {  
        "type": "Property",  
        "value": "123 Main Street, Anytown, USA"  
    },  
    "calendar": {  
        "type": "Property",  
        "value": [  
            "2023-10-01",  
            "2023-10-05",  
            "2023-10-10"  
        ]  
    },  
    "historicalService": {  
        "type": "Property",  
        "value": [  
            "2023-09-15",  
            "2023-09-20",  
            "2023-09-25"  
        ]  
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
