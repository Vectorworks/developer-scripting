# GetDXFColorToLW

## Description
Get DXF color to lineweight

```pascal
FUNCTION GetDXFColorToLW(dxfClrIndex : INTEGER): INTEGER;
```

```python
def vs.GetDXFColorToLW(dxfClrIndex):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dxfClrIndex|INTEGER|   |

## Examples
```pascal
resultN := GetDXFColorToLW(1);
```
```python
import vs

# Get DXF color to lineweight.
dxfClrIndex = 1

resultN = vs.GetDXFColorToLW(dxfClrIndex)
vs.Message('GetDXFColorToLW returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2013

## Category
* [ImportExport](../Categories/ImportExport.md)
