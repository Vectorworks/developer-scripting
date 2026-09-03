# DXFScaleString

## Description
Get DXF scale string

```pascal
FUNCTION DXFScaleString(scale : REAL): STRING;
```

```python
def vs.DXFScaleString(scale):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|scale|REAL|   |

## Examples
```pascal
resultStr := DXFScaleString(1.0);
```
```python
import vs

# Get DXF scale string.
scale = 1.0

text = vs.DXFScaleString(scale)
vs.Message('DXFScaleString returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2013

## Category
* [ImportExport](../Categories/ImportExport.md)
