# Duplicate

## Description
Procedure Duplicate copies the currently selected objects and moves them the specified offset distance.

```pascal
PROCEDURE Duplicate(offset : REAL);
```

```python
def vs.Duplicate(offset):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|offset|REAL|Offset value.|

## Remarks
If user has "Offset Duplications" turned off, Duplicate ignores the x/y.

## Examples
#### VectorScript ####
```pascal
Rect(0,1,1,0);
Duplicate(2,0);
{duplicates the rectangle 2 units right of the original}
```
#### Python ####
```python
vs.Rect(0,1,1,0)
vs.Duplicate(2,0)
#{duplicates the rectangle 2 units right of the original}
```

```pascal
	IF kDebugMode THEN alrtdialog( concat('sub MakeSymbol === Begin Sym ', SymName ) );
	BeginSym(SymName);
	SetSelect(h);
	Duplicate(-xLoc, -yLoc);
	EndSym;
	DelObj(h);
END;

if GetType(temp_h) = 15 then BEGIN {placed symbol}
	found_window := TRUE;
	DSelectAll;
	SetSelect(h);
	Duplicate(0,0);
	round_wall_copy := FSActLayer;
	temp_h := FIn3D(round_wall_copy);
	while temp_h <> nil do BEGIN
		trash_h := NIL;
```
```python
import vs

# Procedure Duplicate copies the currently selected objects and moves them
# the specified offset distance.
offset = 0.0

vs.Duplicate(offset)
```

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
