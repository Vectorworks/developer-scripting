# SetWallWidth

## Description
Procedure SetWallWidth sets the default wall width of the document.

```pascal
PROCEDURE SetWallWidth(widthDistance : REAL);
```

```python
def vs.SetWallWidth(widthDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widthDistance|REAL|New default wall width.|

## Examples
```pascal
BEGIN
	defaultThk := kDefaultThk * GetLScale (ActLayer);
	SetWallWidth (defaultThk);
END

BEGIN
	{Since we're not reading the wall type library anymore, we're not guaranteed of a valid wall width, so check it.}
	IF GetWallWidth <= 0 THEN SetWallWidth(3.5");
	For I := 1 to NumPolyPoints - 1 DO BEGIN
		IF PolyPoints[I].tipe = 3 THEN BEGIN
			pt1 := PolyPoints[I].center;
			pt2 := PolyPoints[I].pt;

end else BEGIN
	wallTypeCnt := 1;
	ALLOCATE wallTypes [1..wallTypeCnt];
	wallTypes[1].name := GetPlugInString(5023);
	SetWallWidth(3.5");
	MoveTo(0, 0);
	WallTo(1, 1);
	h := LNewObj;
	DelObj(h);
```
```python
import vs

# Procedure SetWallWidth sets the default wall width of the document.
widthDistance = 2.0

vs.SetWallWidth(widthDistance)
```

## Version
SetWallWidth is obsolete as of VectorWorks12.0<P>

Availability: from MiniCAD6.0

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
