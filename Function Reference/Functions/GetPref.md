# GetPref

## Description
Function GetPref returns the on-off status of the specified preference item.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
FUNCTION GetPref(prefIndex : INTEGER): BOOLEAN;
```

```python
def vs.GetPref(prefIndex):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|prefIndex|INTEGER|Preference item constant.|

## Examples
#### VectorScript ####
```pascal
SelHandleStatus:=GetPref(17);
```
Example for a shortcut to toggle preference true/false:
```pascal
SetPref(49,not GetPref(49));
```
#### Python ####
```python
SelHandleStatus = vs.GetPref(17)
```

```pascal
BEGIN {Main}
	IF SetUpObject(parmName, parmHand, parmRecordHand, wallHand, saveClass, noneClass) THEN BEGIN
	    bsb := vsoStateGetParamChng(parmHand, widgetID, index, oldVal);
	    bUseSoundVWPref := GetPref(18);
		IF GetPluginString (3001) <> '' THEN AutoClass (parmHand, GetPluginString (3001));
		bVersion22 := ( p__Version >= 2200 ) | ((p__Version = 0) & (IsNewCustomObject(parmName))) ;

SetFPat(lnewobj,1);
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

BEGIN
	isPlanViewRotated := GetPref (92);
	IF isPlanViewRotated THEN
	BEGIN
		VSave ('myTempView00000001');
		SetView (0,0,0,0,0,0);
```
```python
UseDefaultContent = vs.GetPref( 130 )
if not UseDefaultContent:
	vs.SetPref( 130, True )
```

## See Also
[SetPref](SetPref.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
