# SetActSymbol

## Description
Procedure SetActSymbol sets the active symbol for a VectorWorks document.

```pascal
PROCEDURE SetActSymbol(name : STRING);
```

```python
def vs.SetActSymbol(name):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of symbol.|

## Examples
```pascal
BEGIN
	SetActSymbol (tempStr);
	tempH := GetRecord (ActSymDef, 1);
	IF tempH <> NIL THEN
	BEGIN
		numGoodTitleblocks := numGoodTitleblocks + 1;

BEGIN
	SetActSymbol (gTitleBlockName);
	symH := ActSymDef;
	gRecordH := GetRecord (symH, 1);
END;

{ Restore active Symbol }
IF GetObject(actSymName) <> NIL THEN SetActSymbol(actSymName);
```
```python
import vs

# Procedure SetActSymbol sets the active symbol for a VectorWorks document.
name = 'Example'

vs.SetActSymbol(name)
```

## Version
Availability: from All Versions

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
