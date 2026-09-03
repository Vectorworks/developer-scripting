# ExportSTEP

```pascal
FUNCTION ExportSTEP(
				filePath               : DYNARRAY[] of CHAR;
				exportSolidsAsSurfaces : BOOLEAN): BOOLEAN;
```

```python
def vs.ExportSTEP(filePath, exportSolidsAsSurfaces):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|DYNARRAY[] of CHAR|   |
|exportSolidsAsSurfaces|BOOLEAN|   |

## Examples
```pascal
resultOK := ExportSTEP(filePath, TRUE);
```
```python
import vs

filePath = 'C:/Temp'
exportSolidsAsSurfaces = True

ok = vs.ExportSTEP(filePath, exportSolidsAsSurfaces)
if ok:
    vs.Message('ExportSTEP succeeded')
else:
    vs.Message('ExportSTEP failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [File I@O](../Categories/File%20IO.md)
