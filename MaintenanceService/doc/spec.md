<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entity: MaintenanceService  
==========================<!-- /10-Header -->  
<!-- 15-License -->  
[Open License](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/MaintenanceService/LICENSE.md)  
[document generated automatically](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Global description: **Represent a scheduled maintenance operation**  
version: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## List of properties  

<sup><sub>[*] If there is not a type in an attribute is because it could have several types or different formats/patterns</sub></sup>  
- `activityRequiredOfCustomer[array]`: ListProperty. Customer preparation activities for maintenance (To be confirmed by customer).  - `anomalyIndicator[array]`: ListProperty. Technical information about the anomaly (Information on analysis).  - `anomalyType[string]`: Class and Grade of anomaly (Classification referred to the maintenance).  - `costForecast[number]`: Calculated cost of the activity (To be confirmed at the end of maintenance).  - `customerID[string]`: Identify the customer.  - `durationOfOperation[number]`: Working time on system (Number of hours to execute the activity).  - `hasConfiguration[array]`: ListProperty. Machine description.  - `machineAddressLocation[string]`: Machine address (Factory address).  - `machineID[string]`: Identify the system (S/N or Unique Identifier).  - `maintenanceDateScheduled[date]`: Maintenance date proposed (To be confirmed by customer).  - `maintenanceDeadline[date]`: Maintenance required by .. (Last date for optimal action).  - `maintenanceOperator[uri]`: Operator in charge of the activity.  - `maintenanceRequired[array]`: ListProperty. Maintenance Service description (List of activity).  - `requiresComponent[array]`: ListProperty. List of machine components required for the maintenance.  - `type[string]`: The type of the entity (MaintenanceService).  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Required properties  
- `activityRequiredOfCustomer`  - `anomalyIndicator`  - `anomalyType`  - `costForecast`  - `customerID`  - `durationOfOperation`  - `hasConfiguration`  - `id`  - `machineAddressLocation`  - `machineID`  - `maintenanceDateScheduled`  - `maintenanceDeadline`  - `maintenanceOperator`  - `maintenanceRequired`  - `requiresComponent`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Data Model description of properties  
Sorted alphabetically (click for details)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
MaintenanceService:    
  description: Represent a scheduled maintenance operation    
  properties:    
    activityRequiredOfCustomer:    
      description: ListProperty. Customer preparation activities for maintenance (To be confirmed by customer).    
      items:    
        description: Required activities.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    anomalyIndicator:    
      description: ListProperty. Technical information about the anomaly (Information on analysis).    
      items:    
        description: Technical information about the anomaly (Information on analysis).    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    anomalyType:    
      description: Class and Grade of anomaly (Classification referred to the maintenance).    
      type: string    
      x-ngsi:    
        type: Property    
    costForecast:    
      description: Calculated cost of the activity (To be confirmed at the end of maintenance).    
      type: number    
      x-ngsi:    
        type: Property    
    customerID:    
      description: Identify the customer.    
      type: string    
      x-ngsi:    
        type: Property    
    durationOfOperation:    
      description: Working time on system (Number of hours to execute the activity).    
      type: number    
      x-ngsi:    
        type: Property    
    hasConfiguration:    
      description: ListProperty. Machine description.    
      items:    
        description: List of components & options.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    machineAddressLocation:    
      description: Machine address (Factory address).    
      type: string    
      x-ngsi:    
        type: Property    
    machineID:    
      description: Identify the system (S/N or Unique Identifier).    
      type: string    
      x-ngsi:    
        type: Property    
    maintenanceDateScheduled:    
      description: Maintenance date proposed (To be confirmed by customer).    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    maintenanceDeadline:    
      description: Maintenance required by .. (Last date for optimal action).    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    maintenanceOperator:    
      description: Operator in charge of the activity.    
      format: uri    
      type: string    
      x-ngsi:    
        type: Relationship    
    maintenanceRequired:    
      description: ListProperty. Maintenance Service description (List of activity).    
      items:    
        description: Required maintenance activity.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    requiresComponent:    
      description: ListProperty. List of machine components required for the maintenance.    
      items:    
        description: Required machine components.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    type:    
      description: The type of the entity (MaintenanceService).    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - machineID    
    - customerID    
    - machineAddressLocation    
    - hasConfiguration    
    - anomalyType    
    - anomalyIndicator    
    - maintenanceDeadline    
    - maintenanceDateScheduled    
    - maintenanceRequired    
    - maintenanceOperator    
    - requiresComponent    
    - durationOfOperation    
    - activityRequiredOfCustomer    
    - costForecast    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/MaintenanceService/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceService/schema.json    
  x-model-tags: maintenace    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Example payloads    
#### MaintenanceService NGSI-v2 key-values Example    
Here is an example of a MaintenanceService in JSON-LD format as key-values. This is compatible with NGSI-v2 when  using `options=keyValues` and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceService/maintenanceService01",  
    "type": "MaintenanceService",  
    "machineID": "S/N123456789",  
    "customerID": "CUST001",  
    "machineAddressLocation": "123 Factory Street, Anytown, USA",  
    "hasConfiguration": [  
        "MachineComponent:machineComponent01"  
    ],  
    "anomalyType": "ClassA-Grade1",  
    "anomalyIndicator": [  
        "High Temperature",  
        "Unusual Vibration"  
    ],  
    "maintenanceDeadline": "2023-10-20",  
    "maintenanceDateScheduled": "2023-10-19",  
    "maintenanceRequired": [  
        "Replace ComponentA",  
        "Lubricate ComponentB"  
    ],  
    "maintenanceOperator": "ServiceTechnician:serviceTechnician01",  
    "requiresComponent": [  
        "MachineComponent:machineComponent01"  
    ],  
    "durationOfOperation": 4.5,  
    "activityRequiredOfCustomer": [  
        "Clear workstation",  
        "Dispose of WIPs"  
    ],  
    "costForecast": 1000  
}  
```  
</details>  
#### MaintenanceService NGSI-v2 normalized Example    
Here is an example of a MaintenanceService in JSON-LD format as normalized. This is compatible with NGSI-v2 when not using options and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:MaintenanceService:maintenanceService01",  
    "type": "MaintenanceService",  
    "machineID": {  
        "type": "Property",  
        "value": "S/N123456789"  
    },  
    "customerID": {  
        "type": "Property",  
        "value": "CUST001"  
    },  
    "machineAddressLocation": {  
        "type": "Property",  
        "value": "123 Factory Street, Anytown, USA"  
    },  
    "hasConfiguration": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MachineComponent:machineComponent01"  
            }  
        ]  
    },  
    "anomalyType": {  
        "type": "Property",  
        "value": "ClassA-Grade1"  
    },  
    "anomalyIndicator": {  
        "type": "Property",  
        "value": [  
            "High Temperature",  
            "Unusual Vibration"  
        ]  
    },  
    "maintenanceDeadline": {  
        "type": "Property",  
        "value": "2023-10-20"  
    },  
    "maintenanceDateScheduled": {  
        "type": "Property",  
        "value": "2023-10-19"  
    },  
    "maintenanceRequired": {  
        "type": "ListProperty",  
        "value": [  
            "Replace ComponentA",  
            "Lubricate ComponentB"  
        ]  
    },  
    "requiresComponent": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MachineComponent:machineComponent01"  
            }  
        ]  
    },  
    "durationOfOperation": {  
        "type": "Number",  
        "value": 4.5  
    },  
    "activityRequiredOfCustomer": {  
        "type": "ListProperty",  
        "value": [  
            "Clear workstation",  
            "Dispose of WIPs"  
        ]  
    },  
    "costForecast": {  
        "type": "number",  
        "value": 1000  
    }  
}  
```  
</details>  
#### MaintenanceService NGSI-LD key-values Example    
Here is an example of a MaintenanceService in JSON-LD format as key-values. This is compatible with NGSI-LD when  using `options=keyValues` and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceService/maintenanceService01",  
    "type": "MaintenanceService",  
    "machineID": "S/N123456789",  
    "customerID": "CUST001",  
    "machineAddressLocation": "123 Factory Street, Anytown, USA",  
    "hasConfiguration": [  
        "MachineComponent:machineComponent01"  
    ],  
    "anomalyType": "ClassA-Grade1",  
    "anomalyIndicator": [  
        "High Temperature",  
        "Unusual Vibration"  
    ],  
    "maintenanceDeadline": "2023-10-20",  
    "maintenanceDateScheduled": "2023-10-19",  
    "maintenanceRequired": [  
        "Replace ComponentA",  
        "Lubricate ComponentB"  
    ],  
    "maintenanceOperator": "ServiceTechnician:serviceTechnician01",  
    "requiresComponent": [  
        "MachineComponent:machineComponent01"  
    ],  
    "durationOfOperation": 4.5,  
    "activityRequiredOfCustomer": [  
        "Clear workstation",  
        "Dispose of WIPs"  
    ],  
    "costForecast": 1000  
}  
```  
</details>  
#### MaintenanceService NGSI-LD normalized Example    
Here is an example of a MaintenanceService in JSON-LD format as normalized. This is compatible with NGSI-LD when not using options and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/MaintenanceService/maintenanceService01",  
    "type": "MaintenanceService",  
    "machineID": {  
        "type": "Property",  
        "value": "S/N123456789"  
    },  
    "customerID": {  
        "type": "Property",  
        "value": "CUST001"  
    },  
    "machineAddressLocation": {  
        "type": "Property",  
        "value": "123 Factory Street, Anytown, USA"  
    },  
    "hasConfiguration": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MachineComponent:machineComponent01"  
            }  
        ]  
    },  
    "anomalyType": {  
        "type": "Property",  
        "value": "ClassA-Grade1"  
    },  
    "anomalyIndicator": {  
        "type": "ListProperty",  
        "value": [  
            "High Temperature",  
            "Unusual Vibration"  
        ]  
    },  
    "maintenanceDeadline": {  
        "type": "Property",  
        "value": "2023-10-20"  
    },  
    "maintenanceDateScheduled": {  
        "type": "Property",  
        "value": "2023-10-19"  
    },  
    "maintenanceRequired": {  
        "type": "ListProperty",  
        "value": [  
            "Replace ComponentA",  
            "Lubricate ComponentB"  
        ]  
    },  
    "requiresComponent": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MachineComponent:machineComponent01"  
            }  
        ]  
    },  
    "durationOfOperation": {  
        "type": "Property",  
        "value": 4.5  
    },  
    "activityRequiredOfCustomer": {  
        "type": "Property",  
        "value": [  
            "Clear workstation",  
            "Dispose of WIPs"  
        ]  
    },  
    "costForecast": {  
        "type": "Property",  
        "value": 1000  
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
