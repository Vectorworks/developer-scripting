# SetOpacityByClass

## Description
Sets the specified class to use the class opacity.

```pascal
PROCEDURE SetOpacityByClass(h : HANDLE);
```

```python
def vs.SetOpacityByClass(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The object which opacity will be set.|

## Remarks
If you set opacity to an object inside parametric the actual opacity will be combined with the opacity of the parametric object itself. For example a rectangle with 50% opacity inside a parametric with 50% opacity will actually be rendered with 25% opacity. This behavior is the same for symbols too.

## Examples
```pascal
IF ( shadowOpByClass AND ( ( Len( shadowFillName ) = 0 ) OR ( shadowFillStyle <> kShadowByClass ) ) )  THEN SetOpacityByClass( LNewObj )
ELSE SetOpacity ( LNewObj , shadowOpacity );

BEGIN
	SetFillColorByClass(temp_h);
	SetFPatByClass(temp_h);
	SetOpacityByClass(temp_h);
END;
```
```python
	vs.SetLWByClass( objH )
vs.SetMarkerByClass( objH )
vs.SetPenColorByClass( objH )
vs.SetOpacityByClass( objH )
```

## See Also
[GetOpacity](GetOpacity.md) | [SetOpacity](SetOpacity.md) | [GetOpacityByClass](GetOpacityByClass.md) | [SetOpacityByClass](SetOpacityByClass.md)

## Version
Availability: from VectorWorks13.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
