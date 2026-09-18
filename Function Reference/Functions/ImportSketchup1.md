# ImportSketchup1

## Description
Import a sketch up file.

```pascal
FUNCTION ImportSketchup1(
				filePath    : STRING;
				doSingleSym : BOOLEAN): BOOLEAN;
```

```python
def vs.ImportSketchup1(filePath, doSingleSym):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|STRING|   |
|doSingleSym|BOOLEAN|   |

## Examples
```pascal
resultOK := ImportSketchup1('file.txt', TRUE);
```
```python
import vs

# Import a sketch up file.
filePath = 'C:/Temp'
doSingleSym = True

ok = vs.ImportSketchup1(filePath, doSingleSym)
if ok:
    vs.Message('ImportSketchup1 succeeded')
else:
    vs.Message('ImportSketchup1 failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [File I@O](../Categories/File%20IO.md)
