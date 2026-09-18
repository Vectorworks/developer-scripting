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

## Examples
```pascal
resultH := ImportSAT('file.txt', TRUE);
```
```python
import vs

# Import a ACIS SAT 3D model file.
filePath = 'C:/Temp'
doSingleSym = True

objHandle = vs.ImportSAT(filePath, doSingleSym)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2013

## Category
* [File I@O](../Categories/File%20IO.md)
