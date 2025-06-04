# IFC_DMGetPSetFldsCnt

## Description
Gets Fields Count for specified IfcEntry's PSet.

```pascal
FUNCTION IFC_DMGetPSetFldsCnt(
				strObjectName      : STRING;
				strEntryName       : STRING;
				strPSetName        : STRING;
				VAR outFieldsCount : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetPSetFldsCnt(strObjectName, strEntryName, strPSetName):
    return (BOOLEAN, outFieldsCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|outFieldsCount|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
