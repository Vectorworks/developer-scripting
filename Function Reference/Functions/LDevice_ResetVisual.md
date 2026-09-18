# LDevice_ResetVisual

## Description
Cleans up the visual/drawing cache for the specified lighting device object.

```pascal
PROCEDURE LDevice_ResetVisual(h : HANDLE);
```

```python
def vs.LDevice_ResetVisual(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Examples
```pascal
BEGIN
IF DataExchangeSuspend THEN SetRField(LightingDeviceHand,kInstObjName,kNoExport,'True');
LDevice_ResetVisual(LightingDeviceHand);
END;
```
```python
import vs

# Cleans up the visual/drawing cache for the specified lighting device object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.LDevice_ResetVisual(h)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Spotlight](../Categories/Spotlight.md)
