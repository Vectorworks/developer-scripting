# LDevice_Reset

## Description
Reset the specified lighting device object.

```pascal
PROCEDURE LDevice_Reset(h : HANDLE);
```

```python
def vs.LDevice_Reset(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |

## Examples
```pascal
BEGIN
	LDevice_Reset(h);
END;

	END
ELSE
SetRField(InstHandle,kInstObjName,kNoExport,'True'); {Don't export to LW just becaus the user ran refresh instruments}
ResetObject(InstHandle);
LDevice_Reset(InstHandle);
  END;
```
```python
import vs

# Reset the specified lighting device object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.LDevice_Reset(h)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Spotlight](../Categories/Spotlight.md)
