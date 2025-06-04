# IFC_DMGetPSetFldType

## Description
Gets the type of specified Field for IfcEntry's PSet.

```pascal
FUNCTION IFC_DMGetPSetFldType(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				VAR outType   : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetPSetFldType(strObjectName, strEntryName, strPSetName, strFieldName):
    return (BOOLEAN, outType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|outType|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
