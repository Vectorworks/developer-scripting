# IFC_DMSetPSetFldType

## Description
Sets the type of specified Field for IfcEntry's PSet.

```pascal
FUNCTION IFC_DMSetPSetFldType(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				type          : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMSetPSetFldType(strObjectName, strEntryName, strPSetName, strFieldName, type):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|type|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
