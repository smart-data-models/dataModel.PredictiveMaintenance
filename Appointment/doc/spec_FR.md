<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entité : Nomination  
===================<!-- /10-Header -->  
<!-- 15-License -->  
[Licence ouverte] (https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/Appointment/LICENSE.md)  
[document généré automatiquement] (https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Description globale : **Représente un rendez-vous programmé pour l'opérateur**  
version : 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Liste des propriétés  

<sup><sub>[*] S'il n'y a pas de type dans un attribut, c'est parce qu'il peut avoir plusieurs types ou différents formats/modèles</sub></sup>.  
- `appointmentDescription[string]`: La description du rendez-vous.  - `category[string]`: La catégorie du rendez-vous.  - `externalKey[array]`: ListProperty. Les clés externes de cet élément.  - `flag[string]`: Le drapeau du rendez-vous.  - `from[date]`: La date et l'heure de début du rendez-vous.  - `note[string]`: Notes complémentaires pour le rendez-vous.  - `recurring[boolean]`: Indique si le rendez-vous est récurrent.  - `recurringException[string]`: L'exception récurrente pour le rendez-vous.  - `recurringRule[string]`: La règle récurrente pour le rendez-vous.  - `to[date]`: La date et l'heure de fin du rendez-vous.  - `type[string]`: Le type de l'entité (InventoryItem).  - `wholeDay[boolean]`: Indique si le rendez-vous se déroule sur une journée entière.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Propriétés requises  
- `appointmentDescription`  - `category`  - `externalKey`  - `from`  - `id`  - `recurring`  - `to`  - `type`  - `wholeDay`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Modèle de données description des propriétés  
Classés par ordre alphabétique (cliquez pour plus de détails)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
Appointment:    
  description: Represent an scheduled appointment for the operator    
  properties:    
    appointmentDescription:    
      description: The description of the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    category:    
      description: The category of the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    externalKey:    
      description: ListProperty. The external keys for this element.    
      items:    
        description: The external key for this element.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    flag:    
      description: The flag for the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    from:    
      description: The start date and time of the appointment.    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    note:    
      description: Additional notes for the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    recurring:    
      description: Indicates if the appointment is recurring.    
      type: boolean    
      x-ngsi:    
        type: Property    
    recurringException:    
      description: The recurring exception for the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    recurringRule:    
      description: The recurring rule for the appointment.    
      type: string    
      x-ngsi:    
        type: Property    
    to:    
      description: The end date and time of the appointment.    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: The type of the entity (InventoryItem).    
      type: string    
      x-ngsi:    
        type: Property    
    wholeDay:    
      description: Indicates if the appointment is a whole day event.    
      type: boolean    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - externalKey    
    - from    
    - to    
    - wholeDay    
    - recurring    
    - category    
    - appointmentDescription    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/Appointment/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/Appointment/schema.json    
  x-model-tags: maintenance    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Exemples de charges utiles  
#### Nomination Valeurs clés de l'INSG-v2 Exemple  
Voici un exemple de nomination au format JSON-LD en tant que valeurs-clés. Ceci est compatible avec NGSI-v2 lorsque l'on utilise `options=keyValues` et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/Appointment/appointment01",  
    "type": "Appointment",  
    "externalKey": [  
        "F105024",  
        "0000000000 970"  
    ],  
    "from": "2024-08-12",  
    "to": "2024-08-14",  
    "wholeDay": true,  
    "recurring": false,  
    "category": "808080",  
    "appointmentDescription": "EX_Ferie  NO PRESIDIO U-FORM"  
}  
```  
</details>  
#### Rendez-vous NGSI-v2 normalisé Exemple  
Voici un exemple de rendez-vous au format JSON-LD tel qu'il a été normalisé. Ce format est compatible avec les NGSI-v2 lorsqu'il n'utilise pas d'options et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:Appointment:appointment01",  
    "type": "Appointment",  
    "externalKey": {  
        "type": "Property",  
        "value": [  
            "F105024",  
            "0000000000 970"  
        ]  
    },  
    "from": {  
        "type": "Property",  
        "value": "2024-08-12"  
    },  
    "to": {  
        "type": "Property",  
        "value": "2024-08-14"  
    },  
    "wholeDay": {  
        "type": "Property",  
        "value": true  
    },  
    "recurring": {  
        "type": "Property",  
        "value": false  
    },  
    "category": {  
        "type": "Property",  
        "value": "808080"  
    },  
    "appointmentDescription": {  
        "type": "Property",  
        "value": "EX_Ferie  NO PRESIDIO U-FORM"  
    }  
}  
```  
</details>  
#### Nomination valeurs clés NGSI-LD Exemple  
Voici un exemple de nomination au format JSON-LD en tant que valeurs-clés. Ceci est compatible avec NGSI-LD lorsque l'on utilise `options=keyValues` et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/Appointment/appointment01",  
    "type": "Appointment",  
    "externalKey": [  
        "F105024",  
        "0000000000 970"  
    ],  
    "from": "2024-08-12",  
    "to": "2024-08-14",  
    "wholeDay": true,  
    "recurring": false,  
    "category": "808080",  
    "appointmentDescription": "EX_Ferie  NO PRESIDIO U-FORM"  
}  
```  
</details>  
#### Rendez-vous NGSI-LD normalisé Exemple  
Voici un exemple de nomination au format JSON-LD tel que normalisé. Ce format est compatible avec NGSI-LD lorsqu'il n'utilise pas d'options et renvoie les données contextuelles d'une entité individuelle.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/Appointment/appointment01",  
    "type": "Appointment",  
    "externalKey": {  
        "type": "Property",  
        "value": [  
            "F105024",  
            "0000000000 970"  
        ]  
    },  
    "from": {  
        "type": "Property",  
        "value": "2024-08-12"  
    },  
    "to": {  
        "type": "Property",  
        "value": "2024-08-14"  
    },  
    "wholeDay": {  
        "type": "Property",  
        "value": true  
    },  
    "recurring": {  
        "type": "Property",  
        "value": false  
    },  
    "category": {  
        "type": "Property",  
        "value": "808080"  
    },  
    "appointmentDescription": {  
        "type": "Property",  
        "value": "EX_Ferie  NO PRESIDIO U-FORM"  
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
