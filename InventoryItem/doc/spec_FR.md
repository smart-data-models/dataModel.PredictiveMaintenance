<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entité : InventoryItem  
======================<!-- /10-Header -->  
<!-- 15-License -->  
[Licence ouverte] (https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/InventoryItem/LICENSE.md)  
[document généré automatiquement] (https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Description globale : **Représenter un article de l'inventaire à l'intérieur d'un entrepôt**  
version : 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Liste des propriétés  

<sup><sub>[*] S'il n'y a pas de type dans un attribut, c'est parce qu'il peut avoir plusieurs types ou différents formats/modèles</sub></sup>.  
- `availableTotal[integer]`: La quantité totale disponible de l'article.  - `itemLocation[string]`: L'emplacement de l'objet.  - `itemNumber[string]`: L'identifiant unique de l'élément.  - `name[string]`: Le nom de l'élément.  - `netWeight[number]`: Le poids net de l'article.  - `onDelivery[integer]`: La quantité de l'article à la livraison.  - `orderedBooked[integer]`: La quantité de l'article commandé et réservé.  - `physicalAvailability[integer]`: La disponibilité physique de l'article.  - `physicalBooked[integer]`: La quantité physique comptabilisée de l'article.  - `physicalStock[integer]`: Le stock physique de l'article.  - `researchName[string]`: Le nom de recherche de l'élément.  - `site[string]`: Le site où se trouve l'article.  - `totalOrdered[integer]`: La quantité totale commandée pour l'article.  - `type[string]`: Le type de l'entité (InventoryItem).  - `warehouseID[string]`: L'identifiant unique de l'entrepôt.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Propriétés requises  
- `id`  - `itemNumber`  - `physicalStock`  - `type`  - `warehouseID`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Modèle de données description des propriétés  
Classés par ordre alphabétique (cliquez pour plus de détails)  
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
## Exemples de charges utiles  
#### InventoryItem Valeurs clés de l'INS-v2 Exemple  
Voici un exemple d'élément d'inventaire au format JSON-LD en tant que valeurs clés. Ceci est compatible avec NGSI-v2 lorsque l'on utilise `options=keyValues` et renvoie les données contextuelles d'une entité individuelle.  
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
#### InventoryItem NGSI-v2 normalisé Exemple  
Voici un exemple d'élément d'inventaire au format JSON-LD tel qu'il a été normalisé. Ce format est compatible avec la NGSI-v2 lorsqu'il n'utilise pas d'options et renvoie les données contextuelles d'une entité individuelle.  
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
#### InventoryItem Valeurs clés de l'INS-LD Exemple  
Voici un exemple d'élément d'inventaire au format JSON-LD en tant que valeurs clés. Ceci est compatible avec NGSI-LD lorsque l'on utilise `options=keyValues` et renvoie les données contextuelles d'une entité individuelle.  
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
#### InventoryItem NGSI-LD normalisé Exemple  
Voici un exemple d'un InventoryItem au format JSON-LD tel qu'il a été normalisé. Ce format est compatible avec NGSI-LD lorsqu'il n'utilise pas d'options et renvoie les données contextuelles d'une entité individuelle.  
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
Voir [FAQ 10] (https://smartdatamodels.org/index.php/faqs/) pour obtenir une réponse à la question de savoir comment traiter les unités de magnitude.  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
