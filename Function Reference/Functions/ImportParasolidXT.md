# ImportParasolidXT

## Description
Imports the provided Parasolid XT file.

```pascal
FUNCTION ImportParasolidXT(filePath : STRING): BOOLEAN;
```

```python
def vs.ImportParasolidXT(filePath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|STRING|The full path to the file to be imported.|

## Examples
```pascal
resultOK := ImportParasolidXT('file.txt');
```
```python
import vs

# Imports the provided Parasolid XT file.
filePath = 'C:/Temp'

ok = vs.ImportParasolidXT(filePath)
if ok:
    vs.Message('ImportParasolidXT succeeded')
else:
    vs.Message('ImportParasolidXT failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [File I@O](../Categories/File%20IO.md)
