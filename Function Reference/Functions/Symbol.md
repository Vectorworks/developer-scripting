# Symbol

## Description
Procedure Symbol places a symbol in the document at the specified coordinate location.

```pascal
PROCEDURE Symbol(
				symbolName    : STRING;
				pX,pY         : REAL;
				rotationAngle : REAL);
```

```python
def vs.Symbol(symbolName, p, rotationAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symbolName|STRING|Name of symbol.|
|p|REAL|Coordinates of symbol insertion point.|
|rotationAngle|REAL|Rotation angle of symbol, in degrees.|

## Remarks
This doesn't work if [[VS:AngleVar]] is turned on.

Seems to set the documents active symbol definition [CMP]

## Version
Availability: from All Versions

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
