# SetLastDXFImportOpt

## Description
Set Last Used DXF Import Settings

```pascal
FUNCTION SetLastDXFImportOpt(
				selector : INTEGER;
				value    : PROCEDURE): BOOLEAN;
```

```python
def vs.SetLastDXFImportOpt(selector, value):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|value|PROCEDURE|   |

## Examples
```pascal
resultOK := SetLastDXFImportOpt(1, value);
```
```python
import vs

# Set Last Used DXF Import Settings.
selector = 1
value = 'Example'

ok = vs.SetLastDXFImportOpt(selector, value)
if ok:
    vs.Message('SetLastDXFImportOpt succeeded')
else:
    vs.Message('SetLastDXFImportOpt failed')
```

## Version
Availability: from Vectorworks 2013

## Category
* [ImportExport](../Categories/ImportExport.md)
