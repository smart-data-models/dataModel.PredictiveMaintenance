<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entität: MaintenanceRequest  
===========================<!-- /10-Header -->  
<!-- 15-License -->  
[Offene Lizenz](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MaintenanceRequest/LICENSE.md)  
[Dokument automatisch generiert](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Globale Beschreibung: **Ein angeforderter Wartungsvorgang**  
Version: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Liste der Eigenschaften  

<sup><sub>[*] Wenn es für ein Attribut keinen Typ gibt, liegt das daran, dass es mehrere Typen oder unterschiedliche Formate/Muster haben kann</sub></sup>.  
- `analysisDate[date]`: Datum des Endes der Analyse.  - `analysisTimeWindow[object]`: Fenster der Analyse (Kalender & Arbeitszeit).  	- `from[date]`: Datum des Beginns der Analyse.    
	- `to[date]`: Enddatum der Analyse.    
- `anomalyIndicator[array]`: ListeEigenschaft. Technische Informationen über die Anomalie (Informationen zur Analyse).  - `anomalyType[string]`: Klasse und Grad der Anomalie (Klassifizierung bezogen auf die Wartung).  - `customerID[string]`: Identifizieren Sie den Kunden (Actual).  - `durationOfOperation[number]`: Arbeitszeit im System (Anzahl der Stunden für die Ausführung der Tätigkeit).  - `hasConfiguration[array]`: ListeEigenschaft. Beschreibung der Maschine.  - `machineAddressLocation[string]`: Maschinenadresse (Werksadresse).  - `machineID[string]`: Identifizieren Sie das System (S/N oder Unique Identifier).  - `maintenanceDeadline[date]`: Wartung erforderlich bis ... (Letzter Termin für optimale Maßnahmen).  - `maintenanceRequired[array]`: ListProperty. Beschreibung des Wartungsdienstes (Liste der Aktivitäten).  - `requiresComponent[array]`: ListeEigenschaft. Liste der für die Wartung erforderlichen Maschinenkomponenten.  - `requiresSkill[array]`: ListProperty. Liste der erforderlichen technischen Fähigkeiten.  - `type[string]`: Der Typ der Entität (MaintenanceRequest).  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Erforderliche Eigenschaften  
- `anomalyType`  - `customerID`  - `id`  - `machineAddressLocation`  - `machineID`  - `maintenanceDeadline`  - `maintenanceRequired`  - `requiresComponent`  - `requiresSkill`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Datenmodell Beschreibung der Eigenschaften  
Alphabetisch sortiert (für Details anklicken)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
MaintenanceRequest:    
  description: Represent a requested maintenance operation    
  properties:    
    analysisDate:    
      description: Date of the end of analysis.    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    analysisTimeWindow:    
      description: Window of the analysis (Calendar & working time).    
      properties:    
        from:    
          description: Start date of the analysis.    
          format: date    
          type: string    
          x-ngsi:    
            type: Property    
        to:    
          description: End date of the analysis.    
          format: date    
          type: string    
          x-ngsi:    
            type: Property    
      required:    
        - from    
        - to    
      type: object    
      x-ngsi:    
        type: Property    
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
    customerID:    
      description: Identify the customer (Actual).    
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
    maintenanceDeadline:    
      description: Maintenance required by .. (Last date for optimal action).    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
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
    requiresSkill:    
      description: ListProperty. List of technical abilities required.    
      items:    
        description: Technical skill description.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    type:    
      description: The type of the entity (MaintenanceRequest).    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - machineID    
    - customerID    
    - machineAddressLocation    
    - anomalyType    
    - maintenanceDeadline    
    - maintenanceRequired    
    - requiresSkill    
    - requiresComponent    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/MaintenanceRequest/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceRequest/schema.json    
  x-model-tags: maintenance    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Beispiel-Nutzlasten  
#### MaintenanceRequest NGSI-v2 key-values Beispiel  
Hier ist ein Beispiel für einen MaintenanceRequest im JSON-LD-Format als Key-Values. Dies ist mit NGSI-v2 kompatibel, wenn `options=keyValues` verwendet wird und liefert die Kontextdaten einer einzelnen Entität.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceRequest/maintenanceRequest01",  
    "type": "MaintenanceRequest",  
    "machineID": "S/N123456789",  
    "customerID": "CUST001",  
    "machineAddressLocation": "123 Factory Street, Anytown, USA",  
    "analysisDate": "2023-10-15",  
    "analysisTimeWindow": {  
        "from": "2023-10-14",  
        "to": "2023-10-14"  
    },  
    "hasConfiguration": [  
        "MachineComponent:machineComponent01"  
    ],  
    "anomalyType": "ClassA-Grade1",  
    "anomalyIndicator": [  
        "High Temperature",  
        "Unusual Vibration"  
    ],  
    "maintenanceDeadline": "2023-10-20",  
    "maintenanceRequired": [  
        "Replace ComponentA",  
        "Lubricate ComponentB"  
    ],  
    "requiresSkill": [  
        "MaintenanceSkill:maintenanceSkill01"  
    ],  
    "requiresComponent": [  
        "MachineComponent:machineComponent01"  
    ],  
    "durationOfOperation": 4.5  
}  
```  
</details>  
#### MaintenanceRequest NGSI-v2 normalisiert Beispiel  
Hier ist ein Beispiel für einen MaintenanceRequest im JSON-LD-Format in normalisierter Form. Dies ist kompatibel mit NGSI-v2, wenn keine Optionen verwendet werden, und liefert die Kontextdaten einer einzelnen Entität.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:MaintenanceRequest:maintenanceRequest01",  
    "type": "MaintenanceRequest",  
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
    "analysisDate": {  
        "type": "Property",  
        "value": "2023-10-15"  
    },  
    "analysisTimeWindow": {  
        "type": "Property",  
        "value": {  
            "from": {  
                "type": "Property",  
                "value": "2023-10-14"  
            },  
            "to": {  
                "type": "Property",  
                "value": "2023-10-14"  
            }  
        }  
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
    "maintenanceRequired": {  
        "type": "Property",  
        "value": [  
            "Replace ComponentA",  
            "Lubricate ComponentB"  
        ]  
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
    }  
}  
```  
</details>  
#### MaintenanceRequest NGSI-LD key-values Beispiel  
Hier ist ein Beispiel für einen MaintenanceRequest im JSON-LD-Format als Key-Values. Dies ist mit NGSI-LD kompatibel, wenn `options=keyValues` verwendet wird und liefert die Kontextdaten einer einzelnen Entität.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceRequest/maintenanceRequest01",  
    "type": "MaintenanceRequest",  
    "machineID": "S/N123456789",  
    "customerID": "CUST001",  
    "machineAddressLocation": "123 Factory Street, Anytown, USA",  
    "analysisDate": "2023-10-15",  
    "analysisTimeWindow": {  
        "from": "2023-10-14",  
        "to": "2023-10-14"  
    },  
    "hasConfiguration": [  
        "MachineComponent:machineComponent01"  
    ],  
    "anomalyType": "ClassA-Grade1",  
    "anomalyIndicator": [  
        "High Temperature",  
        "Unusual Vibration"  
    ],  
    "maintenanceDeadline": "2023-10-20",  
    "maintenanceRequired": [  
        "Replace ComponentA",  
        "Lubricate ComponentB"  
    ],  
    "requiresSkill": [  
        "MaintenanceSkill:maintenanceSkill01"  
    ],  
    "requiresComponent": [  
        "MachineComponent:machineComponent01"  
    ],  
    "durationOfOperation": 4.5  
}  
```  
</details>  
#### MaintenanceRequest NGSI-LD normalisiert Beispiel  
Hier ist ein Beispiel für einen MaintenanceRequest im JSON-LD-Format in normalisierter Form. Dies ist kompatibel mit NGSI-LD, wenn keine Optionen verwendet werden, und liefert die Kontextdaten einer einzelnen Entität.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceRequest/maintenanceRequest01",  
    "type": "MaintenanceRequest",  
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
    "analysisDate": {  
        "type": "Property",  
        "value": "2023-10-15"  
    },  
    "analysisTimeWindow": {  
        "type": "Property",  
        "value": {  
            "from": {  
                "type": "Property",  
                "value": "2023-10-14"  
            },  
            "to": {  
                "type": "Property",  
                "value": "2023-10-14"  
            }  
        }  
    },  
    "hasConfiguration": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationshiup",  
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
    "maintenanceRequired": {  
        "type": "ListProperty",  
        "value": [  
            "Replace ComponentA",  
            "Lubricate ComponentB"  
        ]  
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
    "durationOfOperation": {  
        "type": "Property",  
        "value": 4.5  
    }  
}  
```  
</details><!-- /80-Examples -->  
<!-- 90-FooterNotes -->  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
Siehe [FAQ 10] (https://smartdatamodels.org/index.php/faqs/), um eine Antwort auf die Frage zu erhalten, wie man mit Größeneinheiten umgeht  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
