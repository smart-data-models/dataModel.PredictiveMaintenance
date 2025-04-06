<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entität: Ernennung  
==================<!-- /10-Header -->  
<!-- 15-License -->  
[Offene Lizenz](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/Appointment/LICENSE.md)  
[Dokument automatisch generiert](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Globale Beschreibung: **Einen geplanten Termin für den Betreiber darstellen**  
Version: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Liste der Eigenschaften  

<sup><sub>[*] Wenn es für ein Attribut keinen Typ gibt, kann es mehrere Typen oder verschiedene Formate/Muster haben</sub></sup>.  
- `appointmentDescription[string]`: Die Beschreibung des Termins.  - `category[string]`: Die Kategorie des Termins.  - `externalKey[array]`: ListeEigenschaft. Die externen Schlüssel für dieses Element.  - `flag[string]`: Die Flagge für den Termin.  - `from[date]`: Das Datum und die Uhrzeit des Beginns des Termins.  - `note[string]`: Zusätzliche Hinweise für den Termin.  - `recurring[boolean]`: Gibt an, ob es sich um einen wiederkehrenden Termin handelt.  - `recurringException[string]`: Die wiederkehrende Ausnahme für den Termin.  - `recurringRule[string]`: Die wiederkehrende Regel für den Termin.  - `to[date]`: Das Enddatum und die Uhrzeit des Termins.  - `type[string]`: Der Typ der Entität (InventoryItem).  - `wholeDay[boolean]`: Gibt an, ob es sich bei dem Termin um ein ganztägiges Ereignis handelt.  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Erforderliche Eigenschaften  
- `appointmentDescription`  - `category`  - `externalKey`  - `from`  - `id`  - `recurring`  - `to`  - `type`  - `wholeDay`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Datenmodell Beschreibung der Eigenschaften  
Alphabetisch sortiert (für Details anklicken)  
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
## Beispiel-Nutzlasten  
#### Ernennung von NGSI-v2-Schlüsselwerten Beispiel  
Hier ist ein Beispiel für eine Ernennung im JSON-LD-Format als Key-Values. Dies ist kompatibel mit NGSI-v2, wenn `options=keyValues` verwendet wird und liefert die Kontextdaten einer einzelnen Entität.  
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
#### Ernennung NGSI-v2 normalisiert Beispiel  
Hier ist ein Beispiel für eine Ernennung im JSON-LD-Format in normalisierter Form. Dies ist kompatibel mit NGSI-v2, wenn keine Optionen verwendet werden, und liefert die Kontextdaten einer einzelnen Entität.  
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
#### Ernennung von NGSI-LD-Schlüsselwerten Beispiel  
Hier ist ein Beispiel für eine Ernennung im JSON-LD-Format als Key-Values. Dies ist mit NGSI-LD kompatibel, wenn `options=keyValues` verwendet wird und liefert die Kontextdaten einer einzelnen Entität.  
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
#### Ernennung NGSI-LD normalisiert Beispiel  
Hier ein Beispiel für eine Ernennung im JSON-LD-Format in normalisierter Form. Dies ist mit NGSI-LD kompatibel, wenn keine Optionen verwendet werden, und liefert die Kontextdaten einer einzelnen Entität.  
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
Siehe [FAQ 10] (https://smartdatamodels.org/index.php/faqs/), um eine Antwort auf die Frage zu erhalten, wie man mit Größeneinheiten umgeht  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
