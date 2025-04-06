<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entità: MachineComponent  
========================<!-- /10-Header -->  
<!-- 15-License -->  
[Licenza aperta](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MachineComponent/LICENSE.md)  
[documento generato automaticamente](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Descrizione globale: **Rappresenta un componente all'interno di una macchina o da sostituire**  
versione: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Elenco delle proprietà  

<sup><sub>[*] Se non c'è un tipo in un attributo è perché potrebbe avere diversi tipi o diversi formati/modelli</sub></sup>.  
- `componentCost[number]`: Costo per il cliente in euro.  - `componentDescription[string]`: Nome del prodotto e breve descrizione, nonché link al sito del fornitore.  - `componentSupplierID[string]`: Codice componente fornitore - Originale.  - `dateGuaranteedDelivery[date]`: Data di disponibilità garantita confermata dal fornitore.  - `deliveryCost[number]`: Costo per il cliente in euro.  - `locationInWarehouse[string]`: Identificare la posizione del componente.  - `measurement[object]`: Le proprietà fisiche del componente  	- `height[object]`: Misura dell'altezza dell'oggetto.    
	- `length[object]`: Lunghezza dell'oggetto.    
	- `weight[object]`: Misura del peso dell'oggetto.    
	- `width[object]`: Misura della larghezza dell'oggetto.    
- `numberOfPiecesAvailable[integer]`: Disponibilità attuale delle scorte nei diversi magazzini.  - `numberOfPiecesOnDelivery[integer]`: Ordine in corso - Informazioni sulla conferma dell'ordine.  - `requiresSkill[array]`: ElencoProprietà. Esperienza e strumenti richiesti.  - `supplierID[string]`: Identificare il fornitore - Contatto e informazioni.  - `type[string]`: Il tipo di entità (MachineComponent).  - `warehouseID[string]`: Identificare i luoghi di stoccaggio, anche presso i clienti dei fornitori di servizi.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Proprietà richieste  
- `componentDescription`  - `componentSupplierID`  - `id`  - `locationInWarehouse`  - `measurement`  - `requiresSkill`  - `supplierID`  - `type`  - `warehouseID`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Modello di dati descrizione delle proprietà  
Ordinati in ordine alfabetico (clicca per i dettagli)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
MachineComponent:    
  description: Represent a component inside a machine or to be replaced    
  properties:    
    componentCost:    
      description: Cost for the customer in Euros.    
      type: number    
      x-ngsi:    
        type: Property    
    componentDescription:    
      description: Product Name and a brief description, also link to supplier site.    
      type: string    
      x-ngsi:    
        type: Property    
    componentSupplierID:    
      description: Supplier Component Code - Original.    
      type: string    
      x-ngsi:    
        type: Property    
    dateGuaranteedDelivery:    
      description: Guaranteed availability date confirmed by supplier.    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    deliveryCost:    
      description: Cost for the customer in Euros.    
      type: number    
      x-ngsi:    
        type: Property    
    locationInWarehouse:    
      description: Identify the component location.    
      type: string    
      x-ngsi:    
        type: Property    
    measurement:    
      description: The physical properties of the component    
      properties:    
        height:    
          description: Height measurement of the object.    
          properties:    
            unit:    
              default: cm    
              description: Unit of measurement for height (e.g., cm, m, in).    
              type: string    
              x-ngsi:    
                type: Property    
            value:    
              description: Height value of the object.    
              type: number    
              x-ngsi:    
                type: Property    
          required:    
            - value    
            - unit    
          type: object    
          x-ngsi:    
            type: Property    
        length:    
          description: Length of the object.    
          properties:    
            unit:    
              default: cm    
              description: Unit of measurement for length (e.g., cm, m, in).    
              type: string    
              x-ngsi:    
                type: Property    
            value:    
              description: Length value of the object.    
              type: number    
              x-ngsi:    
                type: Property    
          required:    
            - value    
            - unit    
          type: object    
          x-ngsi:    
            type: Property    
        weight:    
          description: Weight measurement of the object.    
          properties:    
            unit:    
              default: kg    
              description: Unit of measurement for weight (e.g., kg, lb).    
              type: string    
              x-ngsi:    
                type: Property    
            value:    
              description: Weight value of the object.    
              type: number    
              x-ngsi:    
                type: Property    
          required:    
            - value    
            - unit    
          type: object    
          x-ngsi:    
            type: Property    
        width:    
          description: Width measurement of the object.    
          properties:    
            unit:    
              default: cm    
              description: Unit of measurement for width (e.g., cm, m, in).    
              type: string    
              x-ngsi:    
                type: Property    
            value:    
              description: Width value of the object.    
              type: number    
              x-ngsi:    
                type: Property    
          required:    
            - value    
            - unit    
          type: object    
          x-ngsi:    
            type: Property    
      required:    
        - height    
        - width    
        - length    
        - weight    
      type: object    
      x-ngsi:    
        type: Property    
    numberOfPiecesAvailable:    
      description: Current stock availability in different warehouses.    
      type: integer    
      x-ngsi:    
        type: Property    
    numberOfPiecesOnDelivery:    
      description: Order in progress - Info about order confirmation.    
      type: integer    
      x-ngsi:    
        type: Property    
    requiresSkill:    
      description: ListProperty. Experience and tools required.    
      items:    
        description: Technical skill description.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    supplierID:    
      description: Identify the Supplier - Contact and info.    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: The type of the entity (MachineComponent).    
      type: string    
      x-ngsi:    
        type: Property    
    warehouseID:    
      description: Identify the warehouse places, also c/o customer of service suppliers.    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - componentSupplierID    
    - componentDescription    
    - requiresSkill    
    - supplierID    
    - warehouseID    
    - locationInWarehouse    
    - measurement    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/MachineComponent/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MachineComponent/schema.json    
  x-model-tags: maintenance    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Esempi di payload  
#### MachineComponent Valori chiave NGSI-v2 Esempio  
Ecco un esempio di MachineComponent in formato JSON-LD come valori-chiave. Questo è compatibile con NGSI-v2 quando si usa `options=keyValues` e restituisce i dati di contesto di una singola entità.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceComponent/maintenanceComponent01",  
    "type": "MaintenanceComponent",  
    "componentSupplierID": "SUP12345",  
    "componentDescription": "High-Performance Motor with advanced features and link to supplier site.",  
    "requiresSkill": [  
        "MaintenanceSkill:maintenanceSkill01"  
    ],  
    "supplierID": "SUP001",  
    "warehouseID": "WH001",  
    "locationInWarehouse": "Aisle 5, Shelf 3",  
    "numberOfPiecesAvailable": 50,  
    "numberOfPiecesOnDelivery": 20,  
    "dateGuaranteedDelivery": "2023-12-31",  
    "measurement": {  
        "height": {  
            "value": 10.5,  
            "unit": "cm"  
        },  
        "width": {  
            "value": 15.2,  
            "unit": "cm"  
        },  
        "length": {  
            "value": 20.8,  
            "unit": "cm"  
        },  
        "weight": {  
            "value": 5.5,  
            "unit": "kg"  
        }  
    },  
    "componentCost": 250.75,  
    "deliveryCost": 15.50  
}  
```  
</details>  
#### MachineComponent NGSI-v2 normalizzato Esempio  
Ecco un esempio di MachineComponent in formato JSON-LD normalizzato. Questo è compatibile con NGSI-v2 quando non si utilizzano opzioni e restituisce i dati di contesto di una singola entità.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:MachineComponent:machineComponent01",  
    "type": "MachineComponent",  
    "componentSupplierID": {  
        "type": "Property",  
        "value": "SUP12345"  
    },  
    "componentDescription": {  
        "type": "Property",  
        "value": "High-Performance Motor with advanced features and link to supplier site."  
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
    "supplierID": {  
        "type": "Property",  
        "value": "SUP001"  
    },  
    "warehouseID": {  
        "type": "Property",  
        "value": "WH001"  
    },  
    "locationInWarehouse": {  
        "type": "Property",  
        "value": "Aisle 5, Shelf 3"  
    },  
    "numberOfPiecesAvailable": {  
        "type": "Integer",  
        "value": 50  
    },  
    "numberOfPiecesOnDelivery": {  
        "type": "Integer",  
        "value": 20  
    },  
    "dateGuaranteedDelivery": {  
        "type": "Property",  
        "value": "2023-12-31"  
    },  
    "measurement": {  
        "type": "Property",  
        "value": {  
            "height": {  
                "value": {  
                    "type": "Property",  
                    "value": 10.5  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "width": {  
                "value": {  
                    "type": "Property",  
                    "value": 15.2  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "length": {  
                "value": {  
                    "type": "Property",  
                    "value": 20.8  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "weight": {  
                "value": {  
                    "type": "Property",  
                    "value": 5.5  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "kg"  
                }  
            }  
        }  
    },  
    "componentCost": {  
        "type": "Property",  
        "value": 250.75  
    },  
    "deliveryCost": {  
        "type": "Property",  
        "value": 15.50  
    }  
}  
```  
</details>  
#### MachineComponent Valori chiave NGSI-LD Esempio  
Ecco un esempio di MachineComponent in formato JSON-LD come valori-chiave. Questo è compatibile con NGSI-LD quando si usa `options=keyValues` e restituisce i dati di contesto di una singola entità.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MachineComponent/machineComponent01",  
    "type": "MachineComponent",  
    "componentSupplierID": "SUP12345",  
    "componentDescription": "High-Performance Motor with advanced features and link to supplier site.",  
    "requiresSkill": [  
        "MaintenanceSkill:maintenanceSkill01"  
    ],  
    "supplierID": "SUP001",  
    "warehouseID": "WH001",  
    "locationInWarehouse": "Aisle 5, Shelf 3",  
    "numberOfPiecesAvailable": 50,  
    "numberOfPiecesOnDelivery": 20,  
    "dateGuaranteedDelivery": "2023-12-31",  
    "measurement": {  
        "height": {  
            "value": 10.5,  
            "unit": "cm"  
        },  
        "width": {  
            "value": 15.2,  
            "unit": "cm"  
        },  
        "length": {  
            "value": 20.8,  
            "unit": "cm"  
        },  
        "weight": {  
            "value": 5.5,  
            "unit": "kg"  
        }  
    },  
    "componentCost": 250.75,  
    "deliveryCost": 15.50  
}  
```  
</details>  
#### MacchinaComponente NGSI-LD normalizzata Esempio  
Ecco un esempio di MachineComponent in formato JSON-LD normalizzato. Questo è compatibile con NGSI-LD quando non si usano opzioni e restituisce i dati di contesto di una singola entità.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MachineComponent/machineComponent01",  
    "type": "MachineComponent",  
    "componentSupplierID": {  
        "type": "Property",  
        "value": "SUP12345"  
    },  
    "componentDescription": {  
        "type": "Property",  
        "value": "High-Performance Motor with advanced features and link to supplier site."  
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
    "supplierID": {  
        "type": "Property",  
        "value": "SUP001"  
    },  
    "warehouseID": {  
        "type": "Property",  
        "value": "WH001"  
    },  
    "locationInWarehouse": {  
        "type": "Property",  
        "value": "Aisle 5, Shelf 3"  
    },  
    "numberOfPiecesAvailable": {  
        "type": "Property",  
        "value": 50  
    },  
    "numberOfPiecesOnDelivery": {  
        "type": "Property",  
        "value": 20  
    },  
    "dateGuaranteedDelivery": {  
        "type": "Property",  
        "value": "2023-12-31"  
    },  
    "measurement": {  
        "type": "Property",  
        "value": {  
            "height": {  
                "value": {  
                    "type": "Property",  
                    "value": 10.5  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "width": {  
                "value": {  
                    "type": "Property",  
                    "value": 15.2  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "length": {  
                "value": {  
                    "type": "Property",  
                    "value": 20.8  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "cm"  
                }  
            },  
            "weight": {  
                "value": {  
                    "type": "Property",  
                    "value": 5.5  
                },  
                "unit": {  
                    "type": "Property",  
                    "value": "kg"  
                }  
            }  
        }  
    },  
    "componentCost": {  
        "type": "Property",  
        "value": 250.75  
    },  
    "deliveryCost": {  
        "type": "Property",  
        "value": 15.50  
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
