# DeleteWallSym

## Description
Function DeleteWallSym deletes the referenced symbol from a wall object.

```pascal
FUNCTION DeleteWallSym(symbolHd : HANDLE): BOOLEAN;
```

```python
def vs.DeleteWallSym(symbolHd):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symbolHd|HANDLE|Handle to symbol.|

## Examples
```pascal
resultOK := DeleteWallSym(symbolHd);
```
```python
import vs

# Function DeleteWallSym deletes the referenced symbol from a wall object.
symbolHd = vs.FSActLayer()  # handle to the first selected object on the active layer

ok = vs.DeleteWallSym(symbolHd)
if ok:
    vs.Message('DeleteWallSym succeeded')
else:
    vs.Message('DeleteWallSym failed')
```

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
