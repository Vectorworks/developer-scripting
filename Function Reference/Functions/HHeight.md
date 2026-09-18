# HHeight

## Description
Function HHeight returns the height of the referenced object.

```pascal
FUNCTION HHeight(h : HANDLE): REAL;
```

```python
def vs.HHeight(h):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Observed in 2021: Despite the OIP Width and Height fields flipping values when an object such as a rectangle is rotated 90/-90 degrees, vs.HWidth and vs.HHeight will always return the initial width and height values of the unrotated object, which can lead to unexpected values being returned in some instances. Unsure if this would be considered a bug or a feature...? -AMH (2021.06.26)

## Examples
```pascal
	shapeH := MakeStructuralShape( shapeName, seriesIndex, univSize );
	gStructWidth := HWidth( shapeH );
	gStructDepth := HHeight( shapeH );
IF is3D then BEGIN
	EndXtrd;
	shapeH := LNewObj;
END;

}
	{ get the other properties }
	area   := HArea(objH);
	perim  := HPerim(objH);
	height := HHeight(objH);
	width  := HWidth(objH);

BEGIN
	symbolName := ResList_GetSel( kSymbolsContent );
	symHandle := ResList_ImportItem( kSymbolsContent );
	symbolWidth 	:= HWidth( symHandle );
	symbolHeight	:= HHeight( symHandle );
END;
```
```python
import vs

# Function HHeight returns the height of the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

value = vs.HHeight(h)
vs.Message('HHeight returned: ' + str(value))
```

## Version
Availability: from All Versions

## Category
* [Object Info](../Categories/Object%20Info.md)
