# DSH_GetDSNameAt

## Description
Gets Object's Data Sheet Name for specified index.

```pascal
FUNCTION DSH_GetDSNameAt(
				hObject              : HANDLE;
				VAR dsIndex          : INTEGER;
				VAR outDataSheetName : STRING): BOOLEAN;
```

```python
def vs.DSH_GetDSNameAt(hObject):
    return (BOOLEAN, dsIndex, outDataSheetName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|dsIndex|INTEGER|   |
|outDataSheetName|STRING|   |

## Examples
```pascal
resultOK := DSH_GetDSNameAt(hObject, 1, 'Example');
```
```python
import vs

# Gets Object's Data Sheet Name for specified index.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, dsIndex, outDataSheetName = vs.DSH_GetDSNameAt(hObject)
vs.Message('DSH_GetDSNameAt returned: ' + str((ok, dsIndex, outDataSheetName)))
```

## Version
Availability: from Vectorworks 2020.1

## Category
* [Data Sheets](../Categories/Data%20Sheets.md)
