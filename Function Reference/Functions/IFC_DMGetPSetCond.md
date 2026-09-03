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

## Examples
```pascal
resultOK := IFC_DMGetPSetCond('Example', 'Example', 1, 'Example');
```
```python
import vs

# Returns the Condition for Mapped IfcEntity's Property Set IFC Data Mapping.
strObjectName = 'Example'
strEntryName = 'Example'
psetIndex = 1

ok, outStrPSetCondition = vs.IFC_DMGetPSetCond(strObjectName, strEntryName, psetIndex)
vs.Message('IFC_DMGetPSetCond returned: ' + str((ok, outStrPSetCondition)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
