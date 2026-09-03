# ImportOBJ

## Description
Imports Wavefront (*.obj) files.

```pascal
FUNCTION ImportOBJ(
				fileName    : STRING;
				bAllMatAsRW : BOOLEAN): BOOLEAN;
```

```python
def vs.ImportOBJ(fileName, bAllMatAsRW):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|Full file path.|
|bAllMatAsRW|BOOLEAN|Imports all materials as Renderworks textures.|

## Examples
```pascal
resultOK := ImportOBJ('file.txt', TRUE);
```
```python
import vs

# obj) files.
fileName = 'C:/Temp/example.txt'
bAllMatAsRW = True

ok = vs.ImportOBJ(fileName, bAllMatAsRW)
if ok:
    vs.Message('ImportOBJ succeeded')
else:
    vs.Message('ImportOBJ failed')
```

## Version
Availability: from Vectorworks 2016

## Category
* [ImportExport](../Categories/ImportExport.md)
