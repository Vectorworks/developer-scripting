# CC_Device

## Description
Creates a ConnectCAD device with the given properties. Power should be in W. Weight should be in KG. If make and model match a database entry, database values take precedence. Returns the handle of the created device.

```pascal
FUNCTION CC_Device(
				name        : STRING;
				make        : STRING;
				model       : STRING;
				description : STRING;
				power (W)   : REAL;
				weight (kg) : REAL;
				fieldHeight : REAL;
				fieldWidth  : REAL;
				fieldDepth  : REAL) : HANDLE;
```

```python
def vs.CC_Device(name, make, model, description, power (W), weight (kg), fieldHeight, fieldWidth, fieldDepth):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING||
|make|STRING||
|model|STRING||
|description|STRING||
|power (W)|REAL||
|weight (kg)|REAL||
|fieldHeight|REAL||
|fieldWidth|REAL||
|fieldDepth|REAL||

## Version
Availability: from Vectorworks 2027

## Category
* [ConnectCAD](Categories/ConnectCAD.md)

