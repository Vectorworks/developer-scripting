# HO_GetHoistOriginAt

## Description
Get the name of the Hoist Origin at the given position.

```pascal
FUNCTION HO_GetHoistOriginAt(index : LONGINT): STRING;
```

```python
def vs.HO_GetHoistOriginAt(index):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|LONGINT|   |

## Examples
```pascal
BEGIN
	theOrigName := HO_GetHoistOriginAt( index );
	IF (theOrigName <> 'Drawing Origin') THEN
	BEGIN
		originHdl := GetObject(theOrigName);
		GetSymLoc3D(originHdl,x,y,z);
```
```python
import vs

# Get the name of the Hoist Origin at the given position.
index = 1

text = vs.HO_GetHoistOriginAt(index)
vs.Message('HO_GetHoistOriginAt returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Spotlight](../Categories/Spotlight.md)
