# GetWallPathType

## Description
Gets the path type of a wall.

```pascal
FUNCTION GetWallPathType(wall : HANDLE): INTEGER;
```

```python
def vs.GetWallPathType(wall):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|wall|HANDLE|The wall.|

## Examples
```pascal
retVal := false;
if ( wallH <> NIL ) THEN BEGIN
	objType := GetTypeN( wallH );
	if ( objType = 68 ) THEN BEGIN
		wallPathType := GetWallPathType( wallH );
		if ( wallPathType = kWallPathType_Line ) THEN BEGIN
			retVal := TRUE;
		END;
```
```python
import vs

# Gets the path type of a wall.
wall = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetWallPathType(wall)
vs.Message('GetWallPathType returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2022

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
