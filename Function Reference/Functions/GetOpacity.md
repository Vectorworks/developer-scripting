# GetOpacity

## Description
Gets the opacity of and object. Opacity is obtained as percentage value in range [0-100].

```pascal
PROCEDURE GetOpacity(
				h           : HANDLE;
				VAR opacity : INTEGER);
```

```python
def vs.GetOpacity(h):
    return opacity
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The object which opacity will be get.|
|opacity|INTEGER|Output parameter. Return the object's opacity as percentage value in range [0-100].|

## Remarks
If you set opacity to an object inside parametric the actual opacity will be combined with the opacity of the parametric object itself. For example a rectangle with 50% opacity inside a parametric with 50% opacity will actually be rendered with 25% opacity. This behavior is the same for symbols too.

## Examples
```pascal
GetOpacity( ObjToMatchHand, ObjOpacity );
SetOpacity( ObjHand, ObjOpacity );
{
GetFillIAxisEndPoint( ObjToMatchHand, ImageFillAxisPt.x, ImageFillAxisPt.y );
SetFillIAxisEndPoint( ObjToMatchHand, ImageFillAxisPt.x, ImageFillAxisPt.y );

	{//// this makes sure that no poly is 100% opaque - a VW bug causes 100% opaque polys to have a white line }
	GetOpacity( ObjHand, polyOpacVal );
	IF ( polyOpacVal > 99 ) THEN SetOpacity( ObjHand, 99 );
END;
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
