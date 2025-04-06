<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entidad: MantenimientoHabilidad  
===============================<!-- /10-Header -->  
<!-- 15-License -->  
[Licencia abierta](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MaintenanceSkill/LICENSE.md)  
[documento generado automáticamente](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Descripción global: **Representa una habilidad requerida para una intervención o poseída por un operador**  
versión: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Lista de propiedades  

<sup><sub>[*] Si no hay un tipo en un atributo es porque puede tener varios tipos o diferentes formatos/patrones</sub></sup>.  
- `requiredTool[array]`: ListProperty. Lista de herramientas necesarias para la habilidad.  - `skillDescription[string]`: Descripción de la habilidad.  - `skillDifficulty[string]`: Dificultad de la habilidad.  - `skillName[string]`: Nombre de la habilidad.  - `type[string]`: Tipo de entidad (MaintenanceSkill).  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Propiedades requeridas  
- `id`  - `skillName`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Descripción de las propiedades del modelo de datos  
Ordenados alfabéticamente (pulse para más detalles)  
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
## Ejemplo de carga útil  
#### MaintenanceSkill NGSI-v2 key-values Ejemplo  
Aquí hay un ejemplo de un MaintenanceSkill en formato JSON-LD como key-values. Esto es compatible con NGSI-v2 cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
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
#### MaintenanceSkill NGSI-v2 normalizado Ejemplo  
He aquí un ejemplo de MaintenanceSkill en formato JSON-LD normalizado. Esto es compatible con NGSI-v2 cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
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
#### MaintenanceSkill NGSI-LD key-values Ejemplo  
Aquí hay un ejemplo de un MaintenanceSkill en formato JSON-LD como key-values. Esto es compatible con NGSI-LD cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
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
#### MaintenanceSkill NGSI-LD normalizado Ejemplo  
He aquí un ejemplo de MaintenanceSkill en formato JSON-LD normalizado. Esto es compatible con NGSI-LD cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
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
Consulte [FAQ 10](https://smartdatamodels.org/index.php/faqs/) para obtener una respuesta sobre cómo tratar las unidades de magnitud.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
