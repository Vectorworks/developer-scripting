# SetCallBackInval

## Description
Sets whether or not callbacks should be invalidating portions of the screen that are being changed. This should be used if you need to create temporary objects for calculation purposes and do not want the screen to be redrawn as a result

```pascal
PROCEDURE SetCallBackInval(turnInvalOn : BOOLEAN);
```

```python
def vs.SetCallBackInval(turnInvalOn):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|turnInvalOn|BOOLEAN|   |

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
