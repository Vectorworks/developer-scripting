# WSScript_GetEditObj

## Description
This function must be used inside a worksheet script called by 'RunScriptEdit' worksheet formula. It will return the object being edited when 'WSScript_GetEdit' returns that the script is in edit mode.

```pascal
FUNCTION WSScript_GetEditObj(
				objIndex   : INTEGER;
				VAR outObj : HANDLE): BOOLEAN;
```

```python
def vs.WSScript_GetEditObj(objIndex):
    return (BOOLEAN, outObj)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objIndex|INTEGER|Index to the object to be returned as the script can be called for a set of objects. Will return FALSE if no such object.|
|outObj|HANDLE|Output the object that is being edited.|

## Examples
```pascal
resultOK := WSScript_GetEditObj(1, outObj);
```
```python
import vs

# This function must be used inside a worksheet script called by
# 'RunScriptEdit' worksheet formula.
objIndex = 1

ok, outObj = vs.WSScript_GetEditObj(objIndex)
vs.Message('WSScript_GetEditObj returned: ' + str((ok, outObj)))
```

## See Also
VS Functions:
[WSScript_GetEdit](WSScript_GetEdit.md)

## Version
Availability: from Vectorworks 2021

## Category
* [Worksheets](../Categories/Worksheets.md)
