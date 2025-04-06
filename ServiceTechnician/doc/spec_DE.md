<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entität: ServiceTechniker  
=========================<!-- /10-Header -->  
<!-- 15-License -->  
[Offene Lizenz](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/ServiceTechnician/LICENSE.md)  
[Dokument automatisch generiert](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Globale Beschreibung: **Vertrete einen Instandhalter, der die Dienstleistung erbringt**  
Version: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Liste der Eigenschaften  

<sup><sub>[*] Wenn es für ein Attribut keinen Typ gibt, liegt das daran, dass es mehrere Typen oder unterschiedliche Formate/Muster haben kann</sub></sup>.  
- `calendar[array]`: ListeEigenschaft. Liste der geplanten Aktivitäten.  - `geographicalArea[string]`: Definition des Gebiets und des Standorts.  - `hasSkill[array]`: ListeEigenschaft. Beschreibung der Fähigkeiten und Erfahrungen.  - `historicalService[array]`: ListProperty. Liste der verwalteten Dienste.  - `organization[string]`: Organisation, zu der der Techniker gehört (PRIMA-Niederlassung oder Außenstelle).  - `referenceAddress[string]`: Startposition (Büro und Zuhause).  - `toolProvided[array]`: ListeEigenschaft. Technische Ausrüstung (Spezialausrüstung, die nicht immer für alle Teams zur Verfügung steht).  - `type[string]`: Der Typ der Entität (ServiceTechnician).  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Erforderliche Eigenschaften  
- `calendar`  - `geographicalArea`  - `hasSkill`  - `historicalService`  - `id`  - `organization`  - `referenceAddress`  - `toolProvided`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Datenmodell Beschreibung der Eigenschaften  
Alphabetisch sortiert (für Details anklicken)  
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
## Beispiel-Nutzlasten  
#### ServiceTechniker NGSI-v2 Schlüsselwerte Beispiel  
Hier ist ein Beispiel für einen ServiceTechnician im JSON-LD-Format als Key-Values. Dies ist kompatibel mit NGSI-v2, wenn `options=keyValues` verwendet wird und liefert die Kontextdaten einer einzelnen Entität.  
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
#### ServiceTechniker NGSI-v2 normalisiert Beispiel  
Hier ist ein Beispiel für einen ServiceTechnician im JSON-LD-Format in normalisierter Form. Dies ist kompatibel mit NGSI-v2, wenn keine Optionen verwendet werden, und liefert die Kontextdaten einer einzelnen Entität.  
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
#### ServiceTechniker NGSI-LD Schlüsselwerte Beispiel  
Hier ist ein Beispiel für einen ServiceTechnician im JSON-LD-Format als Key-Values. Dies ist mit NGSI-LD kompatibel, wenn `options=keyValues` verwendet wird und liefert die Kontextdaten einer einzelnen Entität.  
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
#### ServiceTechniker NGSI-LD normalisiert Beispiel  
Hier ist ein Beispiel für einen ServiceTechnician im JSON-LD-Format in normalisierter Form. Dies ist kompatibel mit NGSI-LD, wenn keine Optionen verwendet werden, und liefert die Kontextdaten einer einzelnen Entität.  
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
Siehe [FAQ 10] (https://smartdatamodels.org/index.php/faqs/), um eine Antwort auf die Frage zu erhalten, wie man mit Größeneinheiten umgeht  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
