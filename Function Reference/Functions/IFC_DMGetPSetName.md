# IFC_DMGetPSetName

## Description
Returns the Name for Mapped IfcEntity's Property Set IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetPSetName(
				strObjectName      : STRING;
				strEntryName       : STRING;
				psetIndex          : INTEGER;
				VAR outStrPSetName : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetPSetName(strObjectName, strEntryName, psetIndex):
    return (BOOLEAN, outStrPSetName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|psetIndex|INTEGER|   |
|outStrPSetName|STRING|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
