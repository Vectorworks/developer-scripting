# DSH_SetDSFieldValue

## Description
Sets Object's Data Sheet field value and returns the operation status(disabled/enabled/invisible/black/red).

```pascal
FUNCTION DSH_SetDSFieldValue(
				hObject       : HANDLE;
				dsName        : STRING;
				fieldLabel    : STRING;
				value         : STRING;
				VAR outStatus : INTEGER): BOOLEAN;
```

```python
def vs.DSH_SetDSFieldValue(hObject, dsName, fieldLabel, value):
    return (BOOLEAN, outStatus)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|dsName|STRING|   |
|fieldLabel|STRING|   |
|value|STRING|   |
|outStatus|INTEGER|   |

## Examples
```pascal
resultOK := DSH_SetDSFieldValue(hObject, 'Example', 'MyRecord', 'Example', 1);
```
```python
import vs

# Sets Object's Data Sheet field value and returns the operation
# status(disabled/enabled/invisible/black/red).
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
dsName = 'Example'
fieldLabel = 'MyField'
value = 'Example'

ok, outStatus = vs.DSH_SetDSFieldValue(hObject, dsName, fieldLabel, value)
vs.Message('DSH_SetDSFieldValue returned: ' + str((ok, outStatus)))
```

## Version
Availability: from Vectorworks 2020.1

## Category
* [Data Sheets](../Categories/Data%20Sheets.md)
