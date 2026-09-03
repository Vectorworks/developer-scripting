# GetLastDXFImportOpt

## Description
Get Last Used DXF Import Settings

```pascal
FUNCTION GetLastDXFImportOpt(
				selector : INTEGER;
				value    : PROCEDURE): BOOLEAN;
```

```python
def vs.GetLastDXFImportOpt(selector, value):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|value|PROCEDURE|   |

## Examples
```pascal
resultOK := GetLastDXFImportOpt(1, value);
```
```python
import vs

# Get Last Used DXF Import Settings.
selector = 1
value = 'Example'

ok = vs.GetLastDXFImportOpt(selector, value)
if ok:
    vs.Message('GetLastDXFImportOpt succeeded')
else:
    vs.Message('GetLastDXFImportOpt failed')
```

## Version
Availability: from Vectorworks 2013

## Category
* [ImportExport](../Categories/ImportExport.md)
