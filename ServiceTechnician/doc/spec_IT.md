<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entità: Tecnico dei servizi  
===========================<!-- /10-Header -->  
<!-- 15-License -->  
[Licenza aperta](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/ServiceTechnician/LICENSE.md)  
[documento generato automaticamente](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Descrizione globale: **Rappresenta un operatore di manutenzione che fornisce il servizio**  
versione: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Elenco delle proprietà  

<sup><sub>[*] Se non c'è un tipo in un attributo è perché potrebbe avere diversi tipi o diversi formati/modelli</sub></sup>.  
- `calendar[array]`: ElencoProprietà. Elenco delle attività pianificate.  - `geographicalArea[string]`: Definizione dell'area e della posizione.  - `hasSkill[array]`: ElencoProprietà. Descrizione delle capacità e delle esperienze.  - `historicalService[array]`: ElencoProprietà. Elenco dei servizi gestiti.  - `organization[string]`: Organizzazione di appartenenza del tecnico (filiale PRIMA o ufficio esterno).  - `referenceAddress[string]`: Posizione di partenza (ufficio e casa).  - `toolProvided[array]`: ElencoProprietà. Attrezzature tecniche (attrezzature speciali non sempre fornite a tutte le squadre).  - `type[string]`: Il tipo di entità (ServiceTechnician).  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Proprietà richieste  
- `calendar`  - `geographicalArea`  - `hasSkill`  - `historicalService`  - `id`  - `organization`  - `referenceAddress`  - `toolProvided`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Modello di dati descrizione delle proprietà  
Ordinati in ordine alfabetico (clicca per i dettagli)  
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
## Esempi di payload  
#### Tecnico dei servizi NGSI-v2 valori-chiave Esempio  
Ecco un esempio di un ServiceTechnician in formato JSON-LD come valori-chiave. Questo è compatibile con NGSI-v2 quando si usa `options=keyValues` e restituisce i dati di contesto di una singola entità.  
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
#### Tecnico dei servizi NGSI-v2 normalizzato Esempio  
Ecco un esempio di un ServiceTechnician in formato JSON-LD normalizzato. Questo è compatibile con NGSI-v2 quando non si utilizzano le opzioni e restituisce i dati di contesto di una singola entità.  
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
#### Tecnico dei servizi NGSI-LD valori chiave Esempio  
Ecco un esempio di un ServiceTechnician in formato JSON-LD come valori-chiave. Questo è compatibile con NGSI-LD quando si usa `options=keyValues` e restituisce i dati di contesto di una singola entità.  
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
#### Tecnico dei servizi NGSI-LD normalizzato Esempio  
Ecco un esempio di un ServiceTechnician in formato JSON-LD normalizzato. Questo è compatibile con NGSI-LD quando non si utilizzano opzioni e restituisce i dati di contesto di una singola entità.  
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
Vedere [FAQ 10](https://smartdatamodels.org/index.php/faqs/) per ottenere una risposta su come gestire le unità di grandezza.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
