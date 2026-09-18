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

## Examples
```pascal
resultOK := IFC_GetPsetPropName('Example', 1, 'Example');
```
```python
import vs

# Returns the name of a property for a specified index in a Property Set.
strPsetName = 'Example'
indexProperty = 1

ok, outPsetPropName = vs.IFC_GetPsetPropName(strPsetName, indexProperty)
vs.Message('IFC_GetPsetPropName returned: ' + str((ok, outPsetPropName)))
```

## Version
Availability: from Vectorworks 2022

## Category
* [IFC](../Categories/IFC.md)
