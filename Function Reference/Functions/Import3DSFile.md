# Import3DSFile

## Description
Imports a 3DS file with a given name and position. To import on the original coordinates, set boolean value atOrigCoords to true. Returns true on success.

```pascal
FUNCTION Import3DSFile(
				fileName     : DYNARRAY[] of CHAR;
				atOrigCoords : BOOLEAN;
				positionX    : REAL;
				positionY    : REAL): BOOLEAN;
```

```python
def vs.Import3DSFile(fileName, atOrigCoords, positionX, positionY):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|DYNARRAY[] of CHAR|   |
|atOrigCoords|BOOLEAN|   |
|positionX|REAL|   |
|positionY|REAL|   |

## Examples
```pascal
resultOK := Import3DSFile(fileName, TRUE, 1.0, 2.0);
```
```python
import vs

# Imports a 3DS file with a given name and position.
fileName = 'C:/Temp/example.txt'
atOrigCoords = True
positionX = 1.0
positionY = 2.0

ok = vs.Import3DSFile(fileName, atOrigCoords, positionX, positionY)
if ok:
    vs.Message('Import3DSFile succeeded')
else:
    vs.Message('Import3DSFile failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [ImportExport](../Categories/ImportExport.md)
