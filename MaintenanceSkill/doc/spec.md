<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entity: MaintenanceSkill  
========================<!-- /10-Header -->  
<!-- 15-License -->  
[Open License](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MaintenanceSkill/LICENSE.md)  
[document generated automatically](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Global description: **Represent a skill required for an intervention or possessed by an operator**  
version: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## List of properties  

<sup><sub>[*] If there is not a type in an attribute is because it could have several types or different formats/patterns</sub></sup>  
- `requiredTool[array]`: ListProperty. List of tools required for the skill.  - `skillDescription[string]`: Description of the skill.  - `skillDifficulty[string]`: Difficulty of the skill.  - `skillName[string]`: Name of the skill.  - `type[string]`: The type of the entity (MaintenanceSkill).  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Required properties  
- `id`  - `skillName`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Data Model description of properties  
Sorted alphabetically (click for details)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
MaintenanceSkill:    
  description: Represent a skill required for an intervention or possessed by an operator    
  properties:    
    requiredTool:    
      description: ListProperty. List of tools required for the skill.    
      items:    
        description: Name of the required tool.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    skillDescription:    
      description: Description of the skill.    
      type: string    
      x-ngsi:    
        type: Property    
    skillDifficulty:    
      description: Difficulty of the skill.    
      type: string    
      x-ngsi:    
        type: Property    
    skillName:    
      description: Name of the skill.    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: The type of the entity (MaintenanceSkill).    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - skillName    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/MaintenanceSkill/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceSkill/schema.json    
  x-model-tags: maintenace    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Example payloads    
#### MaintenanceSkill NGSI-v2 key-values Example    
Here is an example of a MaintenanceSkill in JSON-LD format as key-values. This is compatible with NGSI-v2 when  using `options=keyValues` and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:MaintenanceSkill:maintenanceSkill01",  
    "type": "MaintenanceSkill",  
    "skillName": "Engine Repair",  
    "skillDifficulty": "Advanced",  
    "skillDescription": "This skill involves diagnosing and repairing engine issues in vehicles.",  
    "requiredTool": [  
        "Wrench Set",  
        "Socket Set",  
        "OBD-II Scanner",  
        "Jack and Jack Stands"  
    ]  
}  
```  
</details>  
#### MaintenanceSkill NGSI-v2 normalized Example    
Here is an example of a MaintenanceSkill in JSON-LD format as normalized. This is compatible with NGSI-v2 when not using options and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:MaintenanceSkill:maintenanceSkill01",  
    "type": "MaintenanceSkill",  
    "skillName": {  
        "type": "Text",  
        "value": "Engine Repair"  
    },  
    "skillDifficulty": {  
        "type": "Text",  
        "value": "Advanced"  
    },  
    "skillDescription": {  
        "type": "Text",  
        "value": "This skill involves diagnosing and repairing engine issues in vehicles."  
    },  
    "requiredTool": {  
        "type": "Text",  
        "value": [  
            "Wrench Set",  
            "Socket Set",  
            "OBD-II Scanner",  
            "Jack and Jack Stands"  
        ]  
    }  
}  
```  
</details>  
#### MaintenanceSkill NGSI-LD key-values Example    
Here is an example of a MaintenanceSkill in JSON-LD format as key-values. This is compatible with NGSI-LD when  using `options=keyValues` and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceSkill/maintenanceSkill01",  
    "type": "MaintenanceSkill",  
    "skillName": "Engine Repair",  
    "skillDifficulty": "Advanced",  
    "skillDescription": "This skill involves diagnosing and repairing engine issues in vehicles.",  
    "requiredTool": [  
        "Wrench Set",  
        "Socket Set",  
        "OBD-II Scanner",  
        "Jack and Jack Stands"  
    ]  
}  
```  
</details>  
#### MaintenanceSkill NGSI-LD normalized Example    
Here is an example of a MaintenanceSkill in JSON-LD format as normalized. This is compatible with NGSI-LD when not using options and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "type": "MaintenanceSkill",  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceSkill/maintenanceSkill01",  
    "skillName": {  
        "type": "Property",  
        "value": "Engine Repair"  
    },  
    "skillDifficulty": {  
        "type": "Property",  
        "value": "Advanced"  
    },  
    "skillDescription": {  
        "type": "Property",  
        "value": "This skill involves diagnosing and repairing engine issues in vehicles."  
    },  
    "requiredTool": {  
        "type": "ListProperty",  
        "value": [  
            "Wrench Set",  
            "Socket Set",  
            "OBD-II Scanner",  
            "Jack and Jack Stands"  
        ]  
    }  
}  
```  
</details><!-- /80-Examples -->  
<!-- 90-FooterNotes -->  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
See [FAQ 10](https://smartdatamodels.org/index.php/faqs/) to get an answer on how to deal with magnitude units  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
