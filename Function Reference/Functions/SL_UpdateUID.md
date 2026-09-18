# SL_UpdateUID

## Description
Changes an existing UID in the data exchange file.

```pascal
PROCEDURE SL_UpdateUID(
				oldUID : DYNARRAY[] of CHAR;
				newUID : DYNARRAY[] of CHAR);
```

```python
def vs.SL_UpdateUID(oldUID, newUID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|oldUID|DYNARRAY[] of CHAR|   |
|newUID|DYNARRAY[] of CHAR|   |

## Examples
```pascal
BEGIN
	SL_UpdateUID(OldUID,NewUID)
END;
```
```python
import vs

# Changes an existing UID in the data exchange file.
oldUID = 'Example'
newUID = 'Example'

vs.SL_UpdateUID(oldUID, newUID)
```

## Version
Availability: from Vectorworks 2012

## Category
* [Spotlight](../Categories/Spotlight.md)
