# SetDXFColorToLW

## Description
Set DXF color to lineweight

```pascal
PROCEDURE SetDXFColorToLW(
				dxfClrIndex : INTEGER;
				lineWeight  : INTEGER);
```

```python
def vs.SetDXFColorToLW(dxfClrIndex, lineWeight):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dxfClrIndex|INTEGER|   |
|lineWeight|INTEGER|   |

## Examples
```pascal
SetDXFColorToLW(1, 2);
```
```python
import vs

# Set DXF color to lineweight.
dxfClrIndex = 1
lineWeight = 1

vs.SetDXFColorToLW(dxfClrIndex, lineWeight)
```

## Version
Availability: from Vectorworks 2013

## Category
* [ImportExport](../Categories/ImportExport.md)
