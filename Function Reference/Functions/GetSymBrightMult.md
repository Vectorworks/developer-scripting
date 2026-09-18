# GetSymBrightMult

## Description
Function GetSymBrightMult returns the brightness multiplier of the referenced symbol.

The brightness multiplier is used for symbols that contains lights.  This value is a percentage of the symbol definition's light brightness.

```pascal
FUNCTION GetSymBrightMult(symbol : HANDLE): INTEGER;
```

```python
def vs.GetSymBrightMult(symbol):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symbol|HANDLE|Handle to symbol.|

## Remarks
This function returns the brightness multiplier used for symbols that contains lights.  This value is a percentage of the symbol definition's light brightness.

## Examples
```pascal
resultN := GetSymBrightMult(symbol);
```
```python
import vs

# Function GetSymBrightMult returns the brightness multiplier of the
# referenced symbol.
symbol = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetSymBrightMult(symbol)
vs.Message('GetSymBrightMult returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
