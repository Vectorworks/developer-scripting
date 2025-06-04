# IFC_DMSetPSetFldMap

## Description
Sets the Mapping Source of specified Field for IfcEntry's PSet.

```pascal
FUNCTION IFC_DMSetPSetFldMap(
				strObjectName : STRING;
				strEntryName  : STRING;
				strPSetName   : STRING;
				strFieldName  : STRING;
				strMappingSrc : STRING): BOOLEAN;
```

```python
def vs.IFC_DMSetPSetFldMap(strObjectName, strEntryName, strPSetName, strFieldName, strMappingSrc):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|strMappingSrc|STRING|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
