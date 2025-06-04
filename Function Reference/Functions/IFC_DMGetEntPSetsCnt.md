# IFC_DMGetEntPSetsCnt

## Description
Returns the Property Sets count for IfcEntity in Object's IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetEntPSetsCnt(
				strObjectName : STRING;
				strEntryName  : STRING;
				VAR outType   : INTEGER): BOOLEAN;
```

```python
def vs.IFC_DMGetEntPSetsCnt(strObjectName, strEntryName):
    return (BOOLEAN, outType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|outType|INTEGER|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
