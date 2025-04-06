<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entität: InventoryItem  
======================<!-- /10-Header -->  
<!-- 15-License -->  
[Offene Lizenz](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/InventoryItem/LICENSE.md)  
[Dokument automatisch generiert](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Globale Beschreibung: **Stellt einen Artikel des Inventars in einem Lagerhaus dar**  
Version: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Liste der Eigenschaften  

<sup><sub>[*] Wenn es für ein Attribut keinen Typ gibt, kann es mehrere Typen oder verschiedene Formate/Muster haben</sub></sup>.  
- `availableTotal[integer]`: Die gesamte verfügbare Menge des Artikels.  - `itemLocation[string]`: Der Ort, an dem sich das Objekt befindet.  - `itemNumber[string]`: Der eindeutige Bezeichner für den Artikel.  - `name[string]`: Der Name des Artikels.  - `netWeight[number]`: Das Nettogewicht des Artikels.  - `onDelivery[integer]`: Die Menge des Artikels bei Lieferung.  - `orderedBooked[integer]`: Die Menge des bestellten und gebuchten Artikels.  - `physicalAvailability[integer]`: Die physische Verfügbarkeit des Artikels.  - `physicalBooked[integer]`: Die physisch gebuchte Menge der Position.  - `physicalStock[integer]`: Der physische Bestand des Artikels.  - `researchName[string]`: Der Forschungsname des Gegenstands.  - `site[string]`: Der Ort, an dem sich der Artikel befindet.  - `totalOrdered[integer]`: Die Gesamtmenge, die für den Artikel bestellt wurde.  - `type[string]`: Der Typ der Entität (InventoryItem).  - `warehouseID[string]`: Der eindeutige Bezeichner für das Lager.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Erforderliche Eigenschaften  
- `id`  - `itemNumber`  - `physicalStock`  - `type`  - `warehouseID`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Datenmodell Beschreibung der Eigenschaften  
Alphabetisch sortiert (für Details anklicken)  
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
## Beispiel-Nutzlasten  
#### InventoryItem NGSI-v2 key-values Beispiel  
Hier ist ein Beispiel für ein InventoryItem im JSON-LD-Format als Key-Values. Dies ist mit NGSI-v2 kompatibel, wenn `options=keyValues` verwendet wird und gibt die Kontextdaten einer einzelnen Entität zurück.  
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
#### InventoryItem NGSI-v2 normalized Beispiel  
Hier ist ein Beispiel für ein InventoryItem im JSON-LD-Format in normalisierter Form. Dies ist kompatibel mit NGSI-v2, wenn keine Optionen verwendet werden, und liefert die Kontextdaten einer einzelnen Entität.  
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
#### InventoryItem NGSI-LD key-values Beispiel  
Hier ist ein Beispiel für ein InventoryItem im JSON-LD-Format als Key-Values. Dies ist mit NGSI-LD kompatibel, wenn `options=keyValues` verwendet wird und liefert die Kontextdaten einer einzelnen Entität.  
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
#### InventoryItem NGSI-LD normalisiert Beispiel  
Hier ist ein Beispiel für ein InventoryItem im JSON-LD-Format in normalisierter Form. Dies ist mit NGSI-LD kompatibel, wenn keine Optionen verwendet werden, und liefert die Kontextdaten einer einzelnen Entität.  
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
Siehe [FAQ 10] (https://smartdatamodels.org/index.php/faqs/), um eine Antwort auf die Frage zu erhalten, wie man mit Größeneinheiten umgeht  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
