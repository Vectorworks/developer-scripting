# ImportSketchUp

## Description
Imports SketchUp ( *.skp)  files.

```pascal
FUNCTION ImportSketchUp(
				filePath      : STRING;
				bImportAsMesh : BOOLEAN): BOOLEAN;
```

```python
def vs.ImportSketchUp(filePath, bImportAsMesh):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|STRING|Full file path.|
|bImportAsMesh|BOOLEAN|Import as a Mesh or as 3D polys. Mesh = TRUE.|

## Examples
```pascal
resultOK := ImportSketchUp('file.txt', TRUE);
```
```python
import vs

# skp) files.
filePath = 'C:/Temp'
bImportAsMesh = True

ok = vs.ImportSketchUp(filePath, bImportAsMesh)
if ok:
    vs.Message('ImportSketchUp succeeded')
else:
    vs.Message('ImportSketchUp failed')
```

## Version
Availability: from Vectorworks 2016

## Category
* [ImportExport](../Categories/ImportExport.md)
