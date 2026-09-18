# SetMarkerByClass

## Description
Procedure SetMarkerByClass sets the referenced object to use the class attribute marker style.

```pascal
PROCEDURE SetMarkerByClass(h : HANDLE);
```

```python
def vs.SetMarkerByClass(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Sets so that the class arrow style is used for the object referenced by h.

## Examples
```pascal
IF attrNum [6] THEN SetMarkerByClass (objectH)
ELSE IF option = 2 THEN FMarker (mStyle, mSize, mAngle);

BEGIN
	SetFillColorByClass(h);
	SetPenColorByClass(h);
	SetMarkerByClass(h);
	SetFPatByClass(h);
	SetLSByClass(h);
	SetLWByClass(h);
END;

if IsPenColorByClass(h1) then SetPenColorByClass(h2) else BEGIN
	GetPenBack(h1, r, g, b); SetPenBack(h2, r, g, b);
	GetPenFore(h1, r, g, b); SetPenFore(h2, r, g, b);
END;
if IsMarkerByClass(h1) then SetMarkerByClass(h2) else BEGIN
	BSB := GetObjBeginningMarker(h1,style,angle,length,width,thicknessBasis,thickness,visibility);
	BSB := SetObjBeginningMarker(h2,style,angle,length,width,thicknessBasis,thickness,visibility);
	BSB := GetObjEndMarker(h1,style,angle,length,width,thicknessBasis,thickness,visibility);
	BSB := SetObjEndMarker(h2,style,angle,length,width,thicknessBasis,thickness,visibility);
END;
```
```python
if setLineWeight:
	vs.SetLWByClass( objH )
vs.SetMarkerByClass( objH )
vs.SetPenColorByClass( objH )
vs.SetOpacityByClass( objH )
```

## See Also
VS Functions:
[SetObjArrow](SetObjArrow.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
