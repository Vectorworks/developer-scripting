# CC_GetCableTypeData

## Description
Returns the entry in the cable types table for a given cable type. Column 1 = Description, 2 = Outside Diameter

```pascal
FUNCTION CC_GetCableTypeData(
				cable_type : STRING;
				col_index  : INTEGER) : STRING;
```

```python

def vs.CC_GetCableTypeData(cable_type, col_index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|cable_type|STRING||
|col_index|INTEGER||

## Version
Availability: from Vectorworks 2025.2

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)

