# IFC_IsPsetCustom

## Description
Check if Pset is custom.

```pascal
FUNCTION IFC_IsPsetCustom(
				pSetName    : STRING;
				VAR bCustom : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_IsPsetCustom(pSetName):
    return (BOOLEAN, bCustom)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pSetName|STRING|   |
|bCustom|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_IsPsetCustom('Example', TRUE);
```
```python
import vs

# Check if Pset is custom.
pSetName = 'Example'

ok, bCustom = vs.IFC_IsPsetCustom(pSetName)
vs.Message('IFC_IsPsetCustom returned: ' + str((ok, bCustom)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [IFC](../Categories/IFC.md)
