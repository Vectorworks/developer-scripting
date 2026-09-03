# ExportSAT

## Description
Export the selection into a ACIS SAT 3D model file.

```pascal
FUNCTION ExportSAT(
				filePath       : STRING;
				solidAsSurface : BOOLEAN): BOOLEAN;
```

```python
def vs.ExportSAT(filePath, solidAsSurface):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|STRING|Output file path.|
|solidAsSurface|BOOLEAN|   |

## Examples
```pascal
resultOK := ExportSAT('file.txt', TRUE);
```
```python
import vs

# Export the selection into a ACIS SAT 3D model file.
filePath = 'C:/Temp'
solidAsSurface = True

ok = vs.ExportSAT(filePath, solidAsSurface)
if ok:
    vs.Message('ExportSAT succeeded')
else:
    vs.Message('ExportSAT failed')
```

## Version
Availability: from Vectorworks 2013

## Category
* [File I@O](../Categories/File%20IO.md)
