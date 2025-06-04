# DSH_GetDSFieldInfoAt

## Description
Gets Object's Data Sheet field universal and localized sources and label.

```pascal
FUNCTION DSH_GetDSFieldInfoAt(
				hObject        : HANDLE;
				dsName         : STRING;
				VAR fieldIndex : INTEGER;
				VAR outUniSrc  : STRING;
				VAR outLocSrc  : STRING;
				VAR outLabel   : STRING): BOOLEAN;
```

```python
def vs.DSH_GetDSFieldInfoAt(hObject, dsName):
    return (BOOLEAN, fieldIndex, outUniSrc, outLocSrc, outLabel)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|dsName|STRING|   |
|fieldIndex|INTEGER|   |
|outUniSrc|STRING|   |
|outLocSrc|STRING|   |
|outLabel|STRING|   |

## Version
Availability: from Vectorworks 2020.1

## Category
* [Data Sheets](../Categories/Data%20Sheets.md)
