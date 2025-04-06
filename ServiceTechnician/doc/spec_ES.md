<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entidad: ServiceTechnician  
==========================<!-- /10-Header -->  
<!-- 15-License -->  
[Licencia abierta](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/ServiceTechnician/LICENSE.md)  
[documento generado automáticamente](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Descripción global: **Representar a un operador de mantenimiento que presta el servicio**  
versión: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Lista de propiedades  

<sup><sub>[*] Si no hay un tipo en un atributo es porque puede tener varios tipos o diferentes formatos/patrones</sub></sup>.  
- `calendar[array]`: ListProperty. Lista de actividades previstas.  - `geographicalArea[string]`: Definición de la zona y ubicación.  - `hasSkill[array]`: ListaPropiedades. Descripción de capacidades y experiencias.  - `historicalService[array]`: ListProperty. Lista de servicios gestionados.  - `organization[string]`: Organización a la que pertenece el técnico (sucursal PRIMA u oficina externa).  - `referenceAddress[string]`: Posición inicial (oficina y domicilio).  - `toolProvided[array]`: ListProperty. Equipamiento técnico (equipamiento especial que no siempre se proporciona a todos los equipos).  - `type[string]`: El tipo de la entidad (ServiceTechnician).  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Propiedades requeridas  
- `calendar`  - `geographicalArea`  - `hasSkill`  - `historicalService`  - `id`  - `organization`  - `referenceAddress`  - `toolProvided`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Descripción de las propiedades del modelo de datos  
Ordenados alfabéticamente (pulse para más detalles)  
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
## Ejemplo de carga útil  
#### ServiceTechnician NGSI-v2 key-values Ejemplo  
He aquí un ejemplo de un ServiceTechnician en formato JSON-LD como key-values. Esto es compatible con NGSI-v2 cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
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
#### ServiceTechnician NGSI-v2 normalizado Ejemplo  
He aquí un ejemplo de un ServiceTechnician en formato JSON-LD normalizado. Esto es compatible con NGSI-v2 cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
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
#### ServiceTechnician NGSI-LD key-values Ejemplo  
He aquí un ejemplo de un ServiceTechnician en formato JSON-LD como key-values. Esto es compatible con NGSI-LD cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
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
#### Técnico de servicio NGSI-LD normalizado Ejemplo  
He aquí un ejemplo de un ServiceTechnician en formato JSON-LD normalizado. Esto es compatible con NGSI-LD cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
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
Consulte [FAQ 10](https://smartdatamodels.org/index.php/faqs/) para obtener una respuesta sobre cómo tratar las unidades de magnitud.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
