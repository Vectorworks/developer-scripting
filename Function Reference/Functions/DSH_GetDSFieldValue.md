# DSH_GetDSFieldValue

## Description
Gets Object's Data Sheet field value, operation status(disabled/enabled/invisible/black/red), value source type (not set/from instance/from mapping).

```pascal
FUNCTION DSH_GetDSFieldValue(
				hObject       : HANDLE;
				dsName        : STRING;
				fieldLabel    : STRING;
				VAR outValue  : STRING;
				VAR outStatus : INTEGER;
				VAR outType   : INTEGER): BOOLEAN;
```

```python
def vs.DSH_GetDSFieldValue(hObject, dsName, fieldLabel):
    return (BOOLEAN, outValue, outStatus, outType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|dsName|STRING|   |
|fieldLabel|STRING|   |
|outValue|STRING|   |
|outStatus|INTEGER|   |
|outType|INTEGER|   |

## Version
Availability: from Vectorworks 2020.1

## Category
* [Data Sheets](../Categories/Data%20Sheets.md)
