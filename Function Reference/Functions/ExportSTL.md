# ExportSTL

## Description
Export the objects into a STL file.

```pascal
FUNCTION ExportSTL(
				filePath             : STRING;
				exportBinary         : BOOLEAN;
				percentTess          : REAL;
				exportObjectsOptions : INTEGER): BOOLEAN;
```

```python
def vs.ExportSTL(filePath, exportBinary, percentTess, exportObjectsOptions):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|STRING|Output file path.|
|exportBinary|BOOLEAN|binary or ASCII output|
|percentTess|REAL|tessellation resolution -- from 0 to 100  0 -- low, 100 --high|
|exportObjectsOptions|INTEGER|0 -- export visilble objects selected 1 -- export visible objects in activeLayer 2 -- export visible objects in all Layer|

## Remarks
STL is a native file format to the stereolithography CAD software created by 3D Systems.

## Version
Availability: from Vectorworks 2016

## Category
* [File I@O](../Categories/File%20IO.md)
