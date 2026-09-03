# IFC_SetEntityColor

## Description
Sets the default color for an IFC entity type

```pascal
FUNCTION IFC_SetEntityColor(
				inStrIfcType : STRING;
				inRed        : INTEGER;
				inGreen      : INTEGER;
				inBlue       : INTEGER;
				inTransp     : INTEGER): BOOLEAN;
```

```python
def vs.IFC_SetEntityColor(inStrIfcType, inRed, inGreen, inBlue, inTransp):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrIfcType|STRING|   |
|inRed|INTEGER|   |
|inGreen|INTEGER|   |
|inBlue|INTEGER|   |
|inTransp|INTEGER|   |

## Examples
```pascal
resultOK := IFC_SetEntityColor('Example', 1, 2, 3, 10);
```
```python
import vs

# Sets the default color for an IFC entity type.
inStrIfcType = 'Example'
inRed = 0
inGreen = 0
inBlue = 0
inTransp = 1

ok = vs.IFC_SetEntityColor(inStrIfcType, inRed, inGreen, inBlue, inTransp)
if ok:
    vs.Message('IFC_SetEntityColor succeeded')
else:
    vs.Message('IFC_SetEntityColor failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [IFC](../Categories/IFC.md)
