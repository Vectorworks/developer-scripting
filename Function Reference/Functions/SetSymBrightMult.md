# SetSymBrightMult

## Description
Function SetSymBrightMult sets the brightness multiplier for the referenced symbol.

The brightness multiplier is used for symbols that contains lights.  This value is a percentage of the symbol definition's light brightness.

```pascal
PROCEDURE SetSymBrightMult(
				symbol               : HANDLE;
				brightnessMultiplier : INTEGER);
```

```python
def vs.SetSymBrightMult(symbol, brightnessMultiplier):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symbol|HANDLE|Handle to symbol.|
|brightnessMultiplier|INTEGER|Brightness multiplier for symbol.|

## Remarks
This function sets the brightness multiplier used for symbols that contains lights.  This value is a percentage of the symbol definition's light brightness.

## Examples
```pascal
	IF rotX > 90 THEN rotX := 90;
	IF rotX < -90 THEN rotX := -90;
	SET3DRot(LNewObj,rotX,RotY,RotZ,ipX,ipY,0);
	Move3DObj(LNewObj,0,0,ipZ);
	SetSymBrightMult(LNewObj,0);
END;
```
```python
import vs

# Function SetSymBrightMult sets the brightness multiplier for the referenced
# symbol.
symbol = vs.FSActLayer()  # handle to the first selected object on the active layer
brightnessMultiplier = 1

vs.SetSymBrightMult(symbol, brightnessMultiplier)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
