# SetOpacity

## Description
Sets the opacity of the object to the opacity passed in.

```pascal
PROCEDURE SetOpacity(
				h       : HANDLE;
				opacity : INTEGER);
```

```python
def vs.SetOpacity(h, opacity):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Object to which the opacity should be applied.|
|opacity|INTEGER|The opacity value from 0 to 100, where 0 means fully transparent; 100 - fully solid.|

## Remarks
If you set opacity to an object inside parametric the actual opacity will be combined with the opacity of the parametric object itself. For example a rectangle with 50% opacity inside a parametric with 50% opacity will actually be rendered with 25% opacity. This behavior is the same for symbols too.

## Examples
```pascal
SetOpacity(LNewObj, 50);
BeginPoly;
  MoveTo(0.050871161717227",0.047391266048944");
  LineTo(0.050871161717227",0.172590948885572");
  Add2DVertex(0.000871161717227",0.222590948885572",4,0.05");

SetLW(lnewobj,kLightLW);
setobjectvariableint(lnewobj,0,dimstd);
MoveTo(x,y);
LineTo(x2,y2);
SetOpacity(lnewobj, 0);
END;

IF ( shadowOpByClass AND ( ( Len( shadowFillName ) = 0 ) OR ( shadowFillStyle <> kShadowByClass ) ) )  THEN SetOpacityByClass( LNewObj )
ELSE SetOpacity ( LNewObj , shadowOpacity );
```
```python
vs.SetPenFore(objH, vs.GetPenFore(parentH))
start, end, style, size	= vs.GetMarker(parentH)
vs.SetMarker(objH, start, end, style, size)
vs.SetOpacity(objH, vs.GetOpacity(parentH))
```

## See Also
[GetOpacity](GetOpacity.md) | [SetOpacity](SetOpacity.md) | [GetOpacityByClass](GetOpacityByClass.md) | [SetOpacityByClass](SetOpacityByClass.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
