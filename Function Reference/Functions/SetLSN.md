# SetLSN

## Description
Procedure SetLSN sets the linestyle of the referenced object.

If the value is in the range 0 to 71, the specified fill pattern is applied as the linestyle; a negative value will apply the line type resource whose internal index is the negative of the value.

```pascal
PROCEDURE SetLSN(
				h  : HANDLE;
				ls : LONGINT);
```

```python
def vs.SetLSN(h, ls):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|ls|LONGINT|Linestyle to apply to object.|

## Remarks
(\_c\_ 2016.02.29): Expects a name list index, while the older routine [GetLS](GetLS.md) expected a dash style index. 

```pascal
IF GetObject('ISO-02 Dashed') <> NIL THEN
	SetLSN(FSActLayer, -Name2Index('ISO-02 Dashed')); { sets the first selected object to 'ISO-02 Dashed' if the style is present }
```

## Examples
```pascal
MoveTo(X+Overhang,Y);
SetLW(LNewObj,kThinLine);
SetLSN(LNewObj,gDashedLine);
LineTo(X+Overhang, Y+Length+Overhang);
SetLW(LNewObj,kThinLine);
SetLSN(LNewObj,gDashedLine);
	LineTo(X+Depth,Y+Length+Overhang);

BEGIN
	Rect(originX, originY, originX + lngth, originY + thickness);
	SetFPat(LNewObj, 1);
	SetLSN(LNewObj, 0);
END

	dx := wid/2 * .001" * GetLScale(ActLayer)
ELSE dx := 0;
MoveTo(dx,0);
LineTo(pLineLength-dx,0);
SetLSN(lnewobj,2);
SetLW(lnewobj,wid);
IF GetPref(16) THEN	{black background}
	SetPenFore(lnewobj,0,0,0)
ELSE SetPenFore(lnewobj,65535,65535,65535);
```
```python
if setLineWeight:
	vs.SetLW(objH, vs.GetLW(parentH))
vs.SetLSN(objH, vs.GetLSN(parentH))
```

## See Also
VS Functions:
[GetLSN](GetLSN.md)

## Version
Availability: from Vectorworks 2013

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
