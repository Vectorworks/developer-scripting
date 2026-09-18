# SetDrawingRect

## Description
Sets the size of the drawing rectangle.

```pascal
PROCEDURE SetDrawingRect(
				paperWidth  : REAL;
				paperHeight : REAL);
```

```python
def vs.SetDrawingRect(paperWidth, paperHeight):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|paperWidth|REAL|The width of the drawing rectangle|
|paperHeight|REAL|The height of the drawing rectangle|

## Examples
```pascal
BEGIN
	getPrintArea (pageWidth, pageHeight);
	sheetLayerH := CreateLayer (Concat (GetPluginString (3020),'1'), 2);	{"Sheet Layer-1"}
	Layer (GetLName (sheetLayerH));
	SetDrawingRect (pageWidth, pageHeight);
END;

	{drawing size}
	SetDrawingRect  (currDwgWidth , currDwgHeight);
END;

Layer (GetLocStr(16528, 1));
x := 3.25 * getUPI;
y := 3.25 * getUPI;
SetOriginAbsolute (-x, y);
SetDrawingRect (8", 10.33");
DoMenuTextByName (GetLocStr(11050,14), 0);	{'Fit to Page Area'}
```
```python
import vs

# Sets the size of the drawing rectangle.
paperWidth = 2.0
paperHeight = 2.0

vs.SetDrawingRect(paperWidth, paperHeight)
```

## See Also
VS Functions:
[GetDrawingSizeRect](GetDrawingSizeRect.md)

## Version
Availability: from VectorWorks 10.0

## Category
* [Utility](../Categories/Utility.md)
