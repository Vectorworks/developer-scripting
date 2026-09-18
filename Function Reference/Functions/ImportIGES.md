# ImportIGES

## Description
Import a 3D IGES file. (Initial Graphics Exchange Specification)

```pascal
FUNCTION ImportIGES(fileName : STRING): BOOLEAN;
```

```python
def vs.ImportIGES(fileName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|full path to the file for import|

## Examples
```pascal
resultOK := ImportIGES('file.txt');
```
```python
import vs

# Import a 3D IGES file.
fileName = 'C:/Temp/example.txt'

ok = vs.ImportIGES(fileName)
if ok:
    vs.Message('ImportIGES succeeded')
else:
    vs.Message('ImportIGES failed')
```

## See Also
VS Functions:
[ExportIGES](ExportIGES.md)

## Version
Availability: from Vectorworks 2014

## Category
* [File I@O](../Categories/File%20IO.md)
