# GetObjectWallOffset

## Description
Gets an object's offset value in it's break record.

The object (objH) must be contained in wall (wallH) to succeed.

```pascal
FUNCTION GetObjectWallOffset(
				objH       : HANDLE;
				wallH      : HANDLE;
				VAR offset : REAL): BOOLEAN;
```

```python
def vs.GetObjectWallOffset(objH, wallH):
    return (BOOLEAN, offset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|   |
|wallH|HANDLE|   |
|offset|REAL|   |

## Examples
```pascal
BEGIN
	bsb := GetObjectWallOffset( parmHand, wallHand, offsetDist );
	bsb := SetObjectWallOffset( parmHand, wallHand, offsetDist + gLength);
END;

BEGIN
	bsb := GetObjectWallOffset( parmHand, wallHand, offsetDist );
	bsb := SetObjectWallOffset( parmHand, wallHand, offsetDist - abs(gLength));
END;
```
```python
import vs

# Gets an object's offset value in it's break record.
objH = vs.FSActLayer()  # handle to the first selected object on the active layer
wallH = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok, offset = vs.GetObjectWallOffset(objH, wallH)
vs.Message('GetObjectWallOffset returned: ' + str((ok, offset)))
```

## Version
Availability: from Vectorworks 2015

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
