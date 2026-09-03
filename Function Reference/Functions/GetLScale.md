# GetLScale

## Description
Function GetLScale returns the scale of the referenced layer.

```pascal
FUNCTION GetLScale(h : HANDLE): REAL;
```

```python
def vs.GetLScale(h):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Remarks
''Joel Sciamma 2006.02.20'': Returns 200 for 1:200, 1 for 1:1 and 0.5 for 2x

## Examples
#### VectorScript ####
```pascal
LayerScale := GetLScale(LayerHandle);
```
#### Python ####
```python
LayerScale  = vs.GetLScale(vs.ActLayer())
```

```pascal
BEGIN
	GetUnits(fraction, display, format, upi, name, sqName);
	halfFont := kHalfFont * upi * GetLScale(ActLayer);
	tmpAngle := Vec2Ang(segVector);
	tmpVector := 0.5*segVector;
	labelVector := -1 * Perp(UnitVec(tmpVector)) * halfFont;

	END
	ELSE Scaler := GetLScale(ActLayer);
}
	IF GetLayer(parmHand) <> NIL THEN
		Scaler := GetLScale(GetLayer(parmHand))
	ELSE Scaler := GetLScale(ActLayer);

SetFillBack(lnewobj,0);
SetLW(lnewobj,0);
}
IF GetPref (9) THEN	{zoom line thickness}
	dx := wid/2 * .001" * GetLScale(ActLayer)
ELSE dx := 0;
MoveTo(dx,0);
LineTo(pLineLength-dx,0);
SetLSN(lnewobj,2);
SetLW(lnewobj,wid);
```
```python
layerScale = vs.GetLScale( vs.ActLayer() )

containerScale = vs.GetLScale( containerHandle )
```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
