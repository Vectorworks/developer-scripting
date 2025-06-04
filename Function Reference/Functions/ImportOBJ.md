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

## Version
Availability: from Vectorworks 2016

## Category
* [ImportExport](../Categories/ImportExport.md)
