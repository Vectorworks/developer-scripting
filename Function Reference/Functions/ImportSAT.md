# ImportSAT

## Description
Import a ACIS SAT 3D model file.

```pascal
FUNCTION ImportSAT(
				filePath    : STRING;
				doSingleSym : BOOLEAN): HANDLE;
```

```python
def vs.ImportSAT(filePath, doSingleSym):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|STRING|full path to the file for import|
|doSingleSym|BOOLEAN|import the file as a symbol|

## Version
Availability: from Vectorworks 2013

## Category
* [File I@O](../Categories/File%20IO.md)
