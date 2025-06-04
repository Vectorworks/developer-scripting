# IFC_DMSetPSetFldEnbl

## Description
Sets specified Field for IfcEntry's PSet Enabled.

```pascal
FUNCTION IFC_DMSetPSetFldEnbl(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				bEnable       : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMSetPSetFldEnbl(strObjectName, strEntryName, strPSetName, strFieldName, bEnable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|bEnable|BOOLEAN|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
