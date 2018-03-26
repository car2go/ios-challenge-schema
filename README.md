# ios-challenge-schema
## Locations response JSON schema:

```
{
  "type": "array",
  "properties": {
    "locationID": { "type": "integer" },
    "locationName": { "type": "string" },
    "coordinate": {
      "type": "array",
      "properties": {
        "latitude": { "type": "number" },
        "longitute": { "type": "number" }
      }
    }
  } 
}

//dummy example
[
  {
    "locationID": 0,
    "locationName": "hamburg",
    "coordinate": {
      "latitude": 53,
      "longitute": 9
    }
  }
]
```

## Vehicles response JSON schema::

```
{
  "type": "array",
  "properties": {
    "vehicleId": { "type": "integer" },
    "numberPlate": { "type": "string" },
    "locationID": { "type": "integer" },
    "coordinate": {
      "type": "array",
      "properties": {
        "latitude": { "type": "number" },
        "longitute": { "type": "number" }
      }
    },
    "numberOfWheels": { "type": "integer" },
    "fuelLevel": { "type": "string" },
    "modelType": { 
      "type": "string", 
      "enum": ["BCLASS", "SMART"] 
    }
  }
}

//dummy example
[
  {
    "vehicleId": 0,
    "numberPlate": "HH-GO1337",
    "locationID": 0,
    "coordinate": {
      "latitude": 53,
      "longitute": 9
    },
    "numberOfWheels": 3,
    "fuelLevel": 0.7,
    "modelType": "BCLASS"
  }
]
```
