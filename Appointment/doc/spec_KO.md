<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
엔티티: 엔티티: 약속  
============<!-- /10-Header -->  
<!-- 15-License -->  
[오픈 라이선스](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/Appointment/LICENSE.md)  
[문서 자동 생성](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
글로벌 설명: **운영자의 예약된 약속을 나타냅니다**.  
버전: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 속성 목록  

<sup><sub>[*] 속성에 유형이 없는 것은 여러 유형 또는 다른 형식/패턴을 가질 수 있기 때문입니다</sub></sup>.  
- `appointmentDescription[string]`: 약속에 대한 설명입니다.  - `category[string]`: 약속의 카테고리입니다.  - `externalKey[array]`: ListProperty. 이 요소의 외부 키입니다.  - `flag[string]`: 약속의 깃발입니다.  - `from[date]`: 약속의 시작 날짜와 시간입니다.  - `note[string]`: 약속에 대한 추가 참고 사항  - `recurring[boolean]`: 약속이 반복되는지 여부를 나타냅니다.  - `recurringException[string]`: 약속에 대한 반복 예외입니다.  - `recurringRule[string]`: 약속에 대한 반복 규칙입니다.  - `to[date]`: 약속 종료 날짜 및 시간입니다.  - `type[string]`: 엔티티의 유형(인벤토리 항목)입니다.  - `wholeDay[boolean]`: 약속이 하루 종일 진행되는 행사인지 여부를 나타냅니다.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
필수 속성  
- `appointmentDescription`  - `category`  - `externalKey`  - `from`  - `id`  - `recurring`  - `to`  - `type`  - `wholeDay`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 속성에 대한 데이터 모델 설명  
알파벳순으로 정렬(자세한 내용을 보려면 클릭)  
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
## 페이로드 예시  
#### 약속 NGSI-v2 키 값 예시  
다음은 키 값으로 JSON-LD 형식의 약속 예시입니다. 이는 `옵션=키값`을 사용할 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 약속 NGSI-v2 정규화 예제  
다음은 정규화된 JSON-LD 형식의 약속 예시입니다. 이는 옵션을 사용하지 않을 때 NGSI-v2와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 약속 NGSI-LD 키 값 예시  
다음은 키 값으로 JSON-LD 형식의 약속 예시입니다. 이는 `옵션=키값`을 사용할 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
#### 약속 NGSI-LD 정규화 예제  
다음은 정규화된 JSON-LD 형식의 약속 예시입니다. 이는 옵션을 사용하지 않을 때 NGSI-LD와 호환되며 개별 엔티티의 컨텍스트 데이터를 반환합니다.  
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
규모 단위를 다루는 방법에 대한 답변은 [FAQ 10](https://smartdatamodels.org/index.php/faqs/)을 참조하세요.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
