# IsMarkerByClass

## Description
Function IsMarkerByClass returns whether a class marker style is used for the referenced object.

```pascal
FUNCTION IsMarkerByClass(h : HANDLE): BOOLEAN;
```

```python
def vs.IsMarkerByClass(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Returns an indication of whether the class arrow style is used for the object referenced by h.
[sd  8/19/98]

## Examples
```pascal
END;
if not IsLWByClass(objHand) then BEGIN
	PenSize(GetLW(objHand));
END;
if not IsMarkerByClass(objHand) then BEGIN
	MarkerByClass;
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

		{ apply the marker settings to the plug-in }
		IF ((pluginH <> NIL) & (NOT IsMarkerByClass(pluginH))) THEN
			OK := SetObjEndMarker (pluginH, markerStyle, markerAngle, markerSize, markerWidth, markerThkBasis, markerThickness, markerVisibility);
{
message (' ### IsNewCustomObject: markerStyle = ',markerStyle,'    markerSize = ',markerSize);
}
	END	{ of IsNewCustomObject }
```
```python
if not vs.IsMarkerByClass( objHand ):
	vs.MarkerByClass()
```

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
