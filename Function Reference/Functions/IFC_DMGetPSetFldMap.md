# IFC_DMGetPSetFldMap

## Description
Gets the Mapping Source of specified Field for IfcEntry's PSet.

```pascal
FUNCTION IFC_DMGetPSetFldMap(
				strObjectName        : STRING;
				strEntryName         : STRING;
				strPSetName          : STRING;
				strFieldName         : STRING;
				VAR outStrMappingSrc : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetPSetFldMap(strObjectName, strEntryName, strPSetName, strFieldName):
    return (BOOLEAN, outStrMappingSrc)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|strPSetName|STRING|   |
|strFieldName|STRING|   |
|outStrMappingSrc|STRING|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
