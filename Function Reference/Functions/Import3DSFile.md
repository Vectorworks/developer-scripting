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

## Version
Availability: from Vectorworks 2020

## Category
* [ImportExport](../Categories/ImportExport.md)
