# IFC_GetPsetPropName

## Description
Returns the name of a property for a specified index in a Property Set.

```pascal
FUNCTION IFC_GetPsetPropName(
				strPsetName         : STRING;
				indexProperty       : INTEGER;
				VAR outPsetPropName : STRING): BOOLEAN;
```

```python
def vs.IFC_GetPsetPropName(strPsetName, indexProperty):
    return (BOOLEAN, outPsetPropName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strPsetName|STRING|   |
|indexProperty|INTEGER|   |
|outPsetPropName|STRING|   |

## Version
Availability: from Vectorworks 2022

## Category
* [IFC](../Categories/IFC.md)
