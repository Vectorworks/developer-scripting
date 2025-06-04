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

## Version
Availability: from Vectorworks 2020.1

## Category
* [Data Sheets](../Categories/Data%20Sheets.md)
