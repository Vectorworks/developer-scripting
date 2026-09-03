# DSH_GetDSCount

## Description
Gets Data Sheets count for Object.

```pascal
FUNCTION DSH_GetDSCount(
				hObject      : HANDLE;
				VAR outCount : INTEGER): BOOLEAN;
```

```python
def vs.DSH_GetDSCount(hObject):
    return (BOOLEAN, outCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|outCount|INTEGER|   |

## Examples
```pascal
resultOK := DSH_GetDSCount(hObject, 1);
```
```python
import vs

# Gets Data Sheets count for Object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, outCount = vs.DSH_GetDSCount(hObject)
vs.Message('DSH_GetDSCount returned: ' + str((ok, outCount)))
```

## Version
Availability: from Vectorworks 2020.1

## Category
* [Data Sheets](../Categories/Data%20Sheets.md)
