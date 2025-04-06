<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entität: MaintenanceService  
===========================<!-- /10-Header -->  
<!-- 15-License -->  
[Offene Lizenz](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MaintenanceService/LICENSE.md)  
[Dokument automatisch generiert](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Globale Beschreibung: **Ein planmäßiger Wartungsvorgang**  
Version: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Liste der Eigenschaften  

<sup><sub>[*] Wenn es für ein Attribut keinen Typ gibt, liegt das daran, dass es mehrere Typen oder unterschiedliche Formate/Muster haben kann</sub></sup>.  
- `activityRequiredOfCustomer[array]`: ListProperty. Kundenvorbereitungstätigkeiten für die Wartung (vom Kunden zu bestätigen).  - `anomalyIndicator[array]`: ListeEigenschaft. Technische Informationen über die Anomalie (Informationen zur Analyse).  - `anomalyType[string]`: Klasse und Grad der Anomalie (Klassifizierung bezogen auf die Wartung).  - `costForecast[number]`: Berechnete Kosten der Aktivität (am Ende der Wartung zu bestätigen).  - `customerID[string]`: Identifizieren Sie den Kunden.  - `durationOfOperation[number]`: Arbeitszeit im System (Anzahl der Stunden für die Ausführung der Tätigkeit).  - `hasConfiguration[array]`: ListeEigenschaft. Beschreibung der Maschine.  - `machineAddressLocation[string]`: Maschinenadresse (Werksadresse).  - `machineID[string]`: Identifizieren Sie das System (S/N oder Unique Identifier).  - `maintenanceDateScheduled[date]`: Vorgeschlagenes Wartungsdatum (vom Kunden zu bestätigen).  - `maintenanceDeadline[date]`: Wartung erforderlich bis ... (Letzter Termin für optimale Maßnahmen).  - `maintenanceOperator[uri]`: Für die Tätigkeit verantwortlicher Betreiber.  - `maintenanceRequired[array]`: ListProperty. Beschreibung des Wartungsdienstes (Liste der Aktivitäten).  - `requiresComponent[array]`: ListeEigenschaft. Liste der für die Wartung erforderlichen Maschinenkomponenten.  - `type[string]`: Der Typ der Entität (MaintenanceService).  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Erforderliche Eigenschaften  
- `activityRequiredOfCustomer`  - `anomalyIndicator`  - `anomalyType`  - `costForecast`  - `customerID`  - `durationOfOperation`  - `hasConfiguration`  - `id`  - `machineAddressLocation`  - `machineID`  - `maintenanceDateScheduled`  - `maintenanceDeadline`  - `maintenanceOperator`  - `maintenanceRequired`  - `requiresComponent`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Datenmodell Beschreibung der Eigenschaften  
Alphabetisch sortiert (für Details anklicken)  
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
## Beispiel-Nutzlasten  
#### MaintenanceService NGSI-v2 key-values Beispiel  
Hier ist ein Beispiel für einen MaintenanceService im JSON-LD-Format als Key-Values. Dies ist kompatibel mit NGSI-v2 bei Verwendung von `options=keyValues` und liefert die Kontextdaten einer einzelnen Entität.  
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
#### WartungsService NGSI-v2 normalisiert Beispiel  
Hier ist ein Beispiel für einen MaintenanceService im JSON-LD-Format in normalisierter Form. Dies ist kompatibel mit NGSI-v2, wenn keine Optionen verwendet werden, und liefert die Kontextdaten einer einzelnen Entität.  
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
#### MaintenanceService NGSI-LD Schlüsselwerte Beispiel  
Hier ist ein Beispiel für einen MaintenanceService im JSON-LD-Format als Key-Values. Dies ist mit NGSI-LD kompatibel, wenn `options=keyValues` verwendet wird und liefert die Kontextdaten einer einzelnen Entität.  
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
#### WartungsService NGSI-LD normalisiert Beispiel  
Hier ist ein Beispiel für einen MaintenanceService im JSON-LD-Format in normalisierter Form. Dies ist kompatibel mit NGSI-LD, wenn keine Optionen verwendet werden, und liefert die Kontextdaten einer einzelnen Entität.  
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
Siehe [FAQ 10] (https://smartdatamodels.org/index.php/faqs/), um eine Antwort auf die Frage zu erhalten, wie man mit Größeneinheiten umgeht  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
