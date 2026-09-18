# SetPrefReal

## Description
Sets the value of the specified VectorWorks preference setting. Used with preference settings requiring a REAL value.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
PROCEDURE SetPrefReal(
				index : INTEGER;
				value : REAL);
```

```python
def vs.SetPrefReal(index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|Preference item index.|
|value|REAL|New value for preference.|

## Remarks
Sets the value of the specified preference to the value passed.   Similar to SetPref() except it works on preferences for real values

## Examples
#### VectorScript ####
```pascal
SetPrefReal(68,144);
```
#### Python ####
```python

```

```pascal
BEGIN
	SetPrefReal(152, 25.4);
	GetSymLoc(gMyHand, Xpos, Ypos); {get shadow handle's position in case of a custom roof}
	HMove( dpathHandle, -Xpos, -Ypos);
	HRotate( dpathHandle, 0, 0, -objAngle );
	SetPrefReal(152, valUPI);

BEGIN
	SetPrefReal( 500, DocZoomLevel );
	SetVCenter( DocViewCenter.x, DocViewCenter.y );
	Redraw;		{//// Fix for VB-178895 Camera Match Tune View: View not live updating while slider is moving. }
END;
```
```python
vs.SetPrefReal(1, value)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
