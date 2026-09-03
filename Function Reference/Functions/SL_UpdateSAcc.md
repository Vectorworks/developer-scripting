# SL_UpdateSAcc

## Description
Updates an existing Static Accessory UID in the data exchange file.

```pascal
PROCEDURE SL_UpdateSAcc(
				InstHand : HANDLE;
				InstUID  : DYNARRAY[] of CHAR);
```

```python
def vs.SL_UpdateSAcc(InstHand, InstUID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|InstHand|HANDLE|   |
|InstUID|DYNARRAY[] of CHAR|   |

## Examples
```pascal
BEGIN
	SL_UpdateSAcc(InstHandle,InstUID);
END;
```
```python
import vs

# Updates an existing Static Accessory UID in the data exchange file.
InstHand = vs.FSActLayer()  # handle to the first selected object on the active layer
InstUID = 'Example'

vs.SL_UpdateSAcc(InstHand, InstUID)
```

## Version
Availability: from Vectorworks 2012

## Category
* [Spotlight](../Categories/Spotlight.md)
