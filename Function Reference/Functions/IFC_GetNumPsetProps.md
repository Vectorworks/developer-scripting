# IFC_GetNumPsetProps

## Description
Returns the number of properties in a given Property Set

```pascal
FUNCTION IFC_GetNumPsetProps(
				strPsetName     : STRING;
				VAR outNumPsets : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetNumPsetProps(strPsetName):
    return (BOOLEAN, outNumPsets)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strPsetName|STRING|   |
|outNumPsets|INTEGER|   |

## Examples
```pascal
resultOK := IFC_GetNumPsetProps('Example', 1);
```
```python
import vs

# Returns the number of properties in a given Property Set.
strPsetName = 'Example'

ok, outNumPsets = vs.IFC_GetNumPsetProps(strPsetName)
vs.Message('IFC_GetNumPsetProps returned: ' + str((ok, outNumPsets)))
```

## Version
Availability: from Vectorworks 2022

## Category
* [IFC](../Categories/IFC.md)
