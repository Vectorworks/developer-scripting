# IFC_DMGetPSetCond

## Description
Returns the Condition for Mapped IfcEntity's Property Set IFC Data Mapping.

```pascal
FUNCTION IFC_DMGetPSetCond(
				strObjectName           : STRING;
				strEntryName            : STRING;
				psetIndex               : INTEGER;
				VAR outStrPSetCondition : STRING): BOOLEAN;
```

```python
def vs.IFC_DMGetPSetCond(strObjectName, strEntryName, psetIndex):
    return (BOOLEAN, outStrPSetCondition)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strObjectName|STRING|   |
|strEntryName|STRING|   |
|psetIndex|INTEGER|   |
|outStrPSetCondition|STRING|   |

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
