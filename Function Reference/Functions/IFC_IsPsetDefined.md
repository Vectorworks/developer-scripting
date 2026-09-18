# IFC_IsPsetDefined

## Description
Check if the custom Pset exists

```pascal
FUNCTION IFC_IsPsetDefined(strPsetName : STRING): BOOLEAN;
```

```python
def vs.IFC_IsPsetDefined(strPsetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strPsetName|STRING|   |

## Examples
```pascal
resultOK := IFC_IsPsetDefined('Example');
```
```python
import vs

# Check if the custom Pset exists.
strPsetName = 'Example'

ok = vs.IFC_IsPsetDefined(strPsetName)
if ok:
    vs.Message('IFC_IsPsetDefined succeeded')
else:
    vs.Message('IFC_IsPsetDefined failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
