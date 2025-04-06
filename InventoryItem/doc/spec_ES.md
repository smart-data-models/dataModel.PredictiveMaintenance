<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entidad: InventoryItem  
======================<!-- /10-Header -->  
<!-- 15-License -->  
[Licencia abierta](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/InventoryItem/LICENSE.md)  
[documento generado automáticamente](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Descripción global: **Representa un artículo del inventario dentro de un almacén**  
versión: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Lista de propiedades  

<sup><sub>[*] Si no hay un tipo en un atributo es porque puede tener varios tipos o diferentes formatos/patrones</sub></sup>.  
- `availableTotal[integer]`: La cantidad total disponible del artículo.  - `itemLocation[string]`: La ubicación del artículo.  - `itemNumber[string]`: El identificador único del artículo.  - `name[string]`: El nombre del artículo.  - `netWeight[number]`: El peso neto del artículo.  - `onDelivery[integer]`: La cantidad del artículo a la entrega.  - `orderedBooked[integer]`: La cantidad del artículo pedido y reservado.  - `physicalAvailability[integer]`: La disponibilidad física del artículo.  - `physicalBooked[integer]`: La cantidad física contabilizada del artículo.  - `physicalStock[integer]`: Las existencias físicas del artículo.  - `researchName[string]`: El nombre de investigación del artículo.  - `site[string]`: El sitio donde se encuentra el artículo.  - `totalOrdered[integer]`: La cantidad total pedida para el artículo.  - `type[string]`: Tipo de entidad (InventoryItem).  - `warehouseID[string]`: El identificador único del almacén.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Propiedades requeridas  
- `id`  - `itemNumber`  - `physicalStock`  - `type`  - `warehouseID`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Descripción de las propiedades del modelo de datos  
Ordenados alfabéticamente (pulse para más detalles)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
InventoryItem:    
  description: Represent an item of the inventory inside a warehouse    
  properties:    
    availableTotal:    
      description: The total available quantity of the item.    
      type: integer    
      x-ngsi:    
        type: Property    
    itemLocation:    
      description: The location of the item.    
      type: string    
      x-ngsi:    
        type: Property    
    itemNumber:    
      description: The unique identifier for the item.    
      type: string    
      x-ngsi:    
        type: Property    
    name:    
      description: The name of the item.    
      type: string    
      x-ngsi:    
        type: Property    
    netWeight:    
      description: The net weight of the item.    
      type: number    
      x-ngsi:    
        type: Property    
    onDelivery:    
      description: The quantity of the item on delivery.    
      type: integer    
      x-ngsi:    
        type: Property    
    orderedBooked:    
      description: The quantity of the item ordered and booked.    
      type: integer    
      x-ngsi:    
        type: Property    
    physicalAvailability:    
      description: The physical availability of the item.    
      type: integer    
      x-ngsi:    
        type: Property    
    physicalBooked:    
      description: The physical booked quantity of the item.    
      type: integer    
      x-ngsi:    
        type: Property    
    physicalStock:    
      description: The physical stock of the item.    
      type: integer    
      x-ngsi:    
        type: Property    
    researchName:    
      description: The research name of the item.    
      type: string    
      x-ngsi:    
        type: Property    
    site:    
      description: The site where the item is located.    
      type: string    
      x-ngsi:    
        type: Property    
    totalOrdered:    
      description: The total quantity ordered for the item.    
      type: integer    
      x-ngsi:    
        type: Property    
    type:    
      description: The type of the entity (InventoryItem).    
      type: string    
      x-ngsi:    
        type: Property    
    warehouseID:    
      description: The unique identifier for the warehouse.    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - warehouseID    
    - itemNumber    
    - physicalStock    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/InventoryItem/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/InventoryItem/schema.json    
  x-model-tags: maintenance    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Ejemplo de carga útil  
#### InventoryItem NGSI-v2 key-values Ejemplo  
He aquí un ejemplo de un InventoryItem en formato JSON-LD como key-values. Esto es compatible con NGSI-v2 cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/InventoryItem/inventoryItem01",  
    "type": "InventoryItem",  
    "warehouseID": "0000",  
    "itemNumber": "1055.52395.191",  
    "name": "Fusibile SIEMENS 3NA3 807",  
    "physicalStock": 10,  
    "researchName": "FusibileSIEMENS3NA38",  
    "site": "01",  
    "itemLocation": "SILO2/0027",  
    "netWeight": 0.13  
}  
```  
</details>  
#### InventoryItem NGSI-v2 normalized Ejemplo  
He aquí un ejemplo de un InventoryItem en formato JSON-LD normalizado. Esto es compatible con NGSI-v2 cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:InventoryItem:inventoryItem01",  
    "type": "InventoryItem",  
    "warehouseID": {  
        "type": "Property",  
        "value": "0000"  
    },  
    "itemNumber": {  
        "type": "Property",  
        "value": "1055.52395.191"  
    },  
    "name": {  
        "type": "Property",  
        "value": "Fusibile SIEMENS 3NA3 807"  
    },  
    "physicalStock": {  
        "type": "Property",  
        "value": 10  
    },  
    "researchName": {  
        "type": "Property",  
        "value": "FusibileSIEMENS3NA38"  
    },  
    "site": {  
        "type": "Property",  
        "value": "01"  
    },  
    "itemLocation": {  
        "type": "Property",  
        "value": "SILO2/0027"  
    },  
    "netWeight": {  
        "type": "Property",  
        "value": 0.13  
    }  
}  
```  
</details>  
#### InventoryItem NGSI-LD key-values Ejemplo  
He aquí un ejemplo de un InventoryItem en formato JSON-LD como key-values. Esto es compatible con NGSI-LD cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/InventoryItem/inventoryItem01",  
    "type": "InventoryItem",  
    "warehouseID": "0000",  
    "itemNumber": "1055.52395.191",  
    "name": "Fusibile SIEMENS 3NA3 807",  
    "physicalStock": 10,  
    "researchName": "FusibileSIEMENS3NA38",  
    "site": "01",  
    "itemLocation": "SILO2/0027",  
    "netWeight": 0.13  
}  
```  
</details>  
#### InventoryItem NGSI-LD normalizado Ejemplo  
He aquí un ejemplo de un InventoryItem en formato JSON-LD normalizado. Esto es compatible con NGSI-LD cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/InventoryItem/inventoryItem01",  
    "type": "InventoryItem",  
    "warehouseID": {  
        "type": "Property",  
        "value": "0000"  
    },  
    "itemNumber": {  
        "type": "Property",  
        "value": "1055.52395.191"  
    },  
    "name": {  
        "type": "Property",  
        "value": "Fusibile SIEMENS 3NA3 807"  
    },  
    "physicalStock": {  
        "type": "Property",  
        "value": 10  
    },  
    "researchName": {  
        "type": "Property",  
        "value": "FusibileSIEMENS3NA38"  
    },  
    "site": {  
        "type": "Property",  
        "value": "01"  
    },  
    "itemLocation": {  
        "type": "Property",  
        "value": "SILO2/0027"  
    },  
    "netWeight": {  
        "type": "Property",  
        "value": 0.13  
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
