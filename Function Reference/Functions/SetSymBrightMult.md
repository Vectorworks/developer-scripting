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

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
