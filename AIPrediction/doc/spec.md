<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entity: AIPrediction  
====================<!-- /10-Header -->  
<!-- 15-License -->  
[Open License](https://github.com/smart-data-models//dataModel.PredictiveMaintenance/blob/master/AIPrediction/LICENSE.md)  
[document generated automatically](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Global description: **Represent an AI forecasted needed maintenance intervention**  
version: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## List of properties  

<sup><sub>[*] If there is not a type in an attribute is because it could have several types or different formats/patterns</sub></sup>  
- `anomalyType[string]`: Class and Grade of anomaly (Classification referred to the maintenance).  - `computedParameters[array]`: ListProperty. List of computed parameters.  - `country[string]`: The country where the prediction is relevant.  - `date[date]`: The date of the prediction.  - `exceededThreshold[array]`: ListProperty. List of thresholds that have been exceeded.  - `head[string]`: Head-related information.  - `interventionDuration[integer]`: Duration of the intervention in minutes  - `laser[string]`: Laser-related information.  - `maintenanceTypeBin[string]`: Binary representation of the maintenance type.  - `maintenanceTypeDec[integer]`: Decimal representation of the maintenance type.  - `requiresComponent[array]`: ListProperty. List of machine components required for the maintenance.  - `requiresSkill[array]`: ListProperty. Experience and tools required.  - `runningTime[integer]`: Running time in minutes.  - `type[string]`: The type of the entity (InventoryItem).  - `weeksForIntervention[integer]`: Deadline for intervention, in weeks (if anomalyClas is 'Perfect' and this is 52, no intervention is actually required).  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Required properties  
- `anomalyType`  - `computedParameters`  - `date`  - `exceededThreshold`  - `head`  - `id`  - `interventionDuration`  - `laser`  - `maintenanceTypeBin`  - `maintenanceTypeDec`  - `requiresComponent`  - `requiresSkill`  - `runningTime`  - `type`  - `weeksForIntervention`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## Data Model description of properties  
Sorted alphabetically (click for details)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
AIPrediction:    
  description: Represent an AI forecasted needed maintenance intervention    
  properties:    
    anomalyType:    
      description: Class and Grade of anomaly (Classification referred to the maintenance).    
      type: string    
      x-ngsi:    
        type: Property    
    computedParameters:    
      description: ListProperty. List of computed parameters.    
      items:    
        description: The computed parameter with its value.    
        properties:    
          name:    
            description: The parameter's name.    
            type: string    
            x-ngsi:    
              type: Property    
          value:    
            description: The value of the parameter.    
            type: number    
            x-ngsi:    
              type: Property    
        type: object    
        x-ngsi:    
          type: Property    
      type: array    
    country:    
      description: The country where the prediction is relevant.    
      type: string    
      x-ngsi:    
        type: Property    
    date:    
      description: The date of the prediction.    
      format: date    
      type: string    
      x-ngsi:    
        type: Property    
    exceededThreshold:    
      description: ListProperty. List of thresholds that have been exceeded.    
      items:    
        description: The parameter whose threshold has been exceeded.    
        type: string    
        x-ngsi:    
          type: Property    
      type: array    
    head:    
      description: Head-related information.    
      type: string    
      x-ngsi:    
        type: Property    
    interventionDuration:    
      description: Duration of the intervention in minutes    
      type: integer    
      x-ngsi:    
        type: Property    
    laser:    
      description: Laser-related information.    
      type: string    
      x-ngsi:    
        type: Property    
    maintenanceTypeBin:    
      description: Binary representation of the maintenance type.    
      type: string    
      x-ngsi:    
        type: Property    
    maintenanceTypeDec:    
      description: Decimal representation of the maintenance type.    
      type: integer    
      x-ngsi:    
        type: Property    
    requiresComponent:    
      description: ListProperty. List of machine components required for the maintenance.    
      items:    
        description: Required machine components.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    requiresSkill:    
      description: ListProperty. Experience and tools required.    
      items:    
        description: Technical skill description.    
        format: uri    
        type: string    
        x-ngsi:    
          type: Relationship    
      type: array    
    runningTime:    
      description: Running time in minutes.    
      type: integer    
      x-ngsi:    
        type: Property    
    type:    
      description: The type of the entity (InventoryItem).    
      type: string    
      x-ngsi:    
        type: Property    
    weeksForIntervention:    
      description: Deadline for intervention, in weeks (if anomalyClas is 'Perfect' and this is 52, no intervention is actually required).    
      type: integer    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
    - date    
    - laser    
    - head    
    - runningTime    
    - computedParameters    
    - anomalyType    
    - weeksForIntervention    
    - exceededThreshold    
    - maintenanceTypeBin    
    - maintenanceTypeDec    
    - requiresSkill    
    - requiresComponent    
    - interventionDuration    
  type: object    
  x-derived-from: ''    
  x-disclaimer: Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2025 Contributors to Smart Data Models Program    
  x-license-url: https://github.com/smart-data-models/dataModel.PredictiveMaintenance/blob/master/AIPrediction/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.PredictiveMaintenance/AIPrediction/schema.json    
  x-model-tags: maintenance    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Example payloads    
#### AIPrediction NGSI-v2 key-values Example    
Here is an example of a AIPrediction in JSON-LD format as key-values. This is compatible with NGSI-v2 when  using `options=keyValues` and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/AIPrediction/aiPrediction01",  
    "type": "AIPrediction",  
    "country": "Italy",  
    "date": "25/12/2025",  
    "laser": "YLS6000",  
    "head": "T5-Precitec",  
    "runningTime": 1411,  
    "computedParameters": [  
        {  
            "name": "param00",  
            "value": 0.0  
        },  
        {  
            "name": "param01",  
            "value": 0.0  
        },  
        {  
            "name": "param02",  
            "value": 0.0  
        },  
        {  
            "name": "param03",  
            "value": 0.0  
        },  
        {  
            "name": "param04",  
            "value": 0.0  
        },  
        {  
            "name": "param05",  
            "value": 0.0  
        },  
        {  
            "name": "param06",  
            "value": 0.0  
        },  
        {  
            "name": "param07",  
            "value": 1.0  
        },  
        {  
            "name": "param08",  
            "value": 0.0  
        },  
        {  
            "name": "param09",  
            "value": 1.0  
        },  
        {  
            "name": "param10",  
            "value": 1.0  
        },  
        {  
            "name": "param11",  
            "value": 0.0  
        },  
        {  
            "name": "param12",  
            "value": 1.0  
        },  
        {  
            "name": "param13",  
            "value": 0.0  
        }  
    ],  
    "anomalyType": "Near To Fail",  
    "weeksForIntervention": 1,  
    "exceededThreshold": [  
        "Param07",  
        "Param09",  
        "Param10",  
        "Param_12"  
    ],  
    "maintenanceTypeBin": "1011",  
    "maintenanceTypeDec": 11,  
    "requiresSkill": [  
        "MaintenanceSkill:maintenanceSkill01"  
    ],  
    "requiresComponent": [  
        "MachineComponent:machineComponent01"  
    ],  
    "interventionDuration": 19  
}  
```  
</details>  
#### AIPrediction NGSI-v2 normalized Example    
Here is an example of a AIPrediction in JSON-LD format as normalized. This is compatible with NGSI-v2 when not using options and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "id": "urn:ngsi-ld:dataModel.PredictiveMaintenance:AIPrediction:aiPrediction01",  
    "type": "AIPrediction",  
    "country": {  
        "type": "Property",  
        "value": "Italy"  
    },  
    "date": {  
        "type": "Property",  
        "value": "2025-12-25"  
    },  
    "laser": {  
        "type": "Property",  
        "value": "YLS6000"  
    },  
    "head": {  
        "type": "Property",  
        "value": "T5-Precitec"  
    },  
    "runningTime": {  
        "type": "Property",  
        "value": 1411  
    },  
    "computedParameters": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param00"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param01"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param02"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param03"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param04"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param05"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param06"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param07"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param08"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param09"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param10"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param11"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param12"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param13"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            }  
        ]  
    },  
    "anomalyType": {  
        "type": "Property",  
        "value": "Near To Fail"  
    },  
    "weeksForIntervention": {  
        "type": "Property",  
        "value": 1  
    },  
    "exceededThreshold": {  
        "type": "ListProperty",  
        "value": [  
            "param07",  
            "param09",  
            "param10",  
            "param12"  
        ]  
    },  
    "maintenanceTypeBin": {  
        "type": "Property",  
        "value": "1011"  
    },  
    "maintenanceTypeDec": {  
        "type": "Property",  
        "value": 11  
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
    "requiresComponent": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MaintenanceComponent:maintenanceComponent01"  
            }  
        ]  
    },  
    "interventionDuration": {  
        "type": "Property",  
        "value": 19  
    }  
}  
```  
</details>  
#### AIPrediction NGSI-LD key-values Example    
Here is an example of a AIPrediction in JSON-LD format as key-values. This is compatible with NGSI-LD when  using `options=keyValues` and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/AIPrediction/aiPrediction01",  
    "type": "AIPrediction",  
    "country": "Italy",  
    "date": "2025-12-25",  
    "laser": "YLS6000",  
    "head": "T5-Precitec",  
    "runningTime": 1411,  
    "computedParameters": [  
        {  
            "name": "param00",  
            "value": 0.0  
        },  
        {  
            "name": "param01",  
            "value": 0.0  
        },  
        {  
            "name": "param02",  
            "value": 0.0  
        },  
        {  
            "name": "param03",  
            "value": 0.0  
        },  
        {  
            "name": "param04",  
            "value": 0.0  
        },  
        {  
            "name": "param05",  
            "value": 0.0  
        },  
        {  
            "name": "param06",  
            "value": 0.0  
        },  
        {  
            "name": "param07",  
            "value": 1.0  
        },  
        {  
            "name": "param08",  
            "value": 0.0  
        },  
        {  
            "name": "param09",  
            "value": 1.0  
        },  
        {  
            "name": "param10",  
            "value": 1.0  
        },  
        {  
            "name": "param11",  
            "value": 0.0  
        },  
        {  
            "name": "param12",  
            "value": 1.0  
        },  
        {  
            "name": "param13",  
            "value": 0.0  
        }  
    ],  
    "anomalyType": "Near To Fail",  
    "weeksForIntervention": 1,  
    "exceededThreshold": [  
        "Param07",  
        "Param09",  
        "Param10",  
        "Param_12"  
    ],  
    "maintenanceTypeBin": "1011",  
    "maintenanceTypeDec": 11,  
    "requiresSkill": [  
        "MaintenanceSkill:maintenanceSkill01"  
    ],  
    "requiresComponent": [  
        "MachineComponent:machineComponent01"  
    ],  
    "interventionDuration": 19  
}  
```  
</details>  
#### AIPrediction NGSI-LD normalized Example    
Here is an example of a AIPrediction in JSON-LD format as normalized. This is compatible with NGSI-LD when not using options and returns the context data of an individual entity.  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
    "@context": [  
        "https://smartdatamodels.org/context.jsonld"  
    ],  
    "id": "https://smart-data-models.github.io/dataModel.PredictiveMaintenance/AIPrediction/aiPrediction01",  
    "type": "AIPrediction",  
    "country": {  
        "type": "Property",  
        "value": "Italy"  
    },  
    "date": {  
        "type": "Property",  
        "value": "2025-12-25"  
    },  
    "laser": {  
        "type": "Property",  
        "value": "YLS6000"  
    },  
    "head": {  
        "type": "Property",  
        "value": "T5-Precitec"  
    },  
    "runningTime": {  
        "type": "Property",  
        "value": 1411  
    },  
    "computedParameters": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param00"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param01"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param02"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param03"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param04"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param05"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param06"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param07"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param08"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param09"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param10"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param11"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param12"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 1.0  
                }  
            },  
            {  
                "name": {  
                    "type": "Property",  
                    "value": "param13"  
                },  
                "value": {  
                    "type": "Property",  
                    "value": 0.0  
                }  
            }  
        ]  
    },  
    "anomalyType": {  
        "type": "Property",  
        "value": "Near To Fail"  
    },  
    "weeksForIntervention": {  
        "type": "Property",  
        "value": 1  
    },  
    "exceededThreshold": {  
        "type": "Property",  
        "value": [  
            "Param07",  
            "Param09",  
            "Param10",  
            "Param_12"  
        ]  
    },  
    "maintenanceTypeBin": {  
        "type": "Property",  
        "value": "1011"  
    },  
    "maintenanceTypeDec": {  
        "type": "Property",  
        "value": 11  
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
    "requiresComponent": {  
        "type": "ListProperty",  
        "value": [  
            {  
                "type": "Relationship",  
                "id": "MachineComponent:machineComponent01"  
            }  
        ]  
    },  
    "interventionDuration": {  
        "type": "Property",  
        "value": 19  
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
