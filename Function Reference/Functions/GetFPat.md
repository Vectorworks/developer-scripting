# GetFPat

## Description
Function GetFPat returns the fill pattern of the referenced object.

A positive value corresponds to the index of the fill pattern on the pattern palette. A negative value corresponds to internal index of a vector fill pattern applied to the object.

Fill patterns and their associated constants can be found in the [VectorScript Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#fill-patterns).

```pascal
FUNCTION GetFPat(h : HANDLE): LONGINT;
```

```python
def vs.GetFPat(h):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
The negative values need to be converted to positive values for Index2Name to work.

## Examples
#### VectorScript ####
```pascal
FPatValue:=GetFPat(HandleToObj);
```
#### Python ####
```python
FPatValue = vs.GetFPat(HandleToObj)
```

```pascal
		SetFPat(pluginH, 0);
	END;
END
ELSE
IF (GetFPat(pluginH) <> 0) THEN
BEGIN
	Rect(originX, originY, originX + lngth, originY + thickness);
	SetLSN(LNewObj, 0);
END

BEGIN
	patID := GetFPat(parentHand);
	IF patID < 0 THEN
	BEGIN
		resHand	:= GetObject(Index2Name(-patID));
		resType	:= GetTypeN(resHand);

	Moveto(Sin(angle)*rad,cos(angle)*rad);
	CreateText(anno);
	SetTextJust(LNewObj,2);
	SetTextVerticalAlign(LNewObj,3);
	setfpat(lnewobj,GetFPat(parmHand));
	GetFillBack(parmHand,red,grn,bl);
	SetFillBack(LNewObj,red,grn,bl);
	popattrs;
END;
```
```python
nFillPat = vs.GetFPat( hObjectHand )
if nFillPat != 0:
	if vs.IsFPatByClass(gObjHandle):
		vs.SetFPatByClass(hObjectHand)
	else:

if not vs.IsFPatByClass( objHand ):
	penPat	= vs.GetFPat( objHand )
	vs.FillPat( penPat )

if t != vs.kLineNode and t != vs.kLocusNode and t != vs.kLocus3DNode and t != vs.kGroupNode:
	vs.SetFPat(objH, vs.GetFPat(parentH))
```

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
