# GetUnits

## Description
Procedure GetUnits returns the current units settings of the document.

* Table - Units Formats

| Units Format | Constant |
|--------------|----------|
| Decimal | 0 |
| Fractional | 1 |
| Decimal Ft/Inches | 2 |
| Fractional Ft/Inches | 3 |

More extensive Units information is available using the [GetPref](GetPref.md) routines with the selectors shown in the tables of the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md#primary-units-selectors).

```pascal
PROCEDURE GetUnits(
				VAR fraction   : LONGINT;
				VAR display    : LONGINT;
				VAR format     : INTEGER;
				VAR upi        : REAL;
				VAR name       : STRING;
				VAR squareName : STRING);
```

```python
def vs.GetUnits():
    return (fraction, display, format, upi, name, squareName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fraction|LONGINT|Approximate WorldCoords per drawing unit.  Use GetPrefReal(150) instead.|
|display|LONGINT|Returns display accuracy.|
|format|INTEGER|Returns units format setting.|
|upi|REAL|Returns units per inch value.|
|name|STRING|Returns unit mark.|
|squareName|STRING|Returns square unit mark.|

## Remarks
Another way to get the UPI is to use:
UPI := GetPrefReal(152);

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR 
fraction   :LONGINT; 
display    :LONGINT; 
format     :INTEGER; 
upi        :REAL; 
name       :STRING;
squareName :STRING;
BEGIN
GetUnits(fraction, display, format, upi, name, squareName);
Message(fraction, ' ', display, ' ', format, ' ', upi, ' ', name, ' ', squareName);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	fraction, display, format, upi, name, squareName = vs.GetUnits()
	vs.Message(fraction, ' ', display, ' ', format, ' ', upi, ' ', name, ' ', squareName)

Example()
```

```pascal
BEGIN
	GetUnits(fraction, display, format, upi, name, sqName);
	halfFont := kHalfFont * upi * GetLScale(ActLayer);
	tmpAngle := Vec2Ang(segVector);
	tmpVector := 0.5*segVector;
	labelVector := -1 * Perp(UnitVec(tmpVector)) * halfFont;

Height:= pHeight;
GetUnits(Frac, DispAcc,Format,unitsPerInch,UnitMk,SqrUnitMk);
IF pInt_Frame_W < 0 THEN BEGIN
	IF bUseSoundVWPref THEN
		SysBeep;
	SetRField(parmHand, 'Base Cabinet', 'Int Frame W', Num2Str(9,UnitsPerInch));

BEGIN
	GetUnits(DummyInteger,DummyInteger,DummyInteger,UPI,DummyString,DummyString);
END;
```
```python
frac, dispAcc, format	= 0, 0, 0
unitsPerInch			= 0.0
unitMk, sqrUnitMk		= '', ''
frac, dispAcc, format, unitsPerInch, unitMk, sqrUnitMk = vs.GetUnits()
gDTM					= kDTM * unitsPerInch
curbHeight				= vs.PCurb_Height

fraction, display, format = 0, 0, 0
unitsPerInch = 0.0
unit, sqrUnit = '', ''
fraction, display, format, unitsPerInch, unit, sqrUnit = vs.GetUnits()
global gDTM
gDTM	= unitsPerInch * kDTM

frac, dispAcc, format = 0, 0, 0
unitsPerInch = 0.0
unitMk, sqrUnitMk = '', ''
frac, dispAcc, format, unitsPerInch, unitMk, sqrUnitMk = vs.GetUnits()
if vs.PDraw_Gutter_Curb:
	guterCurb = vs.PCurb_Width + vs.PGutter_Width + vs.PGutter_Fence_Offset
else:
	guterCurb = vs.PGutter_Width + vs.PGutter_Fence_Offset
```

## Version
Availability: from All Versions

## Category
* [Units](../Categories/Units.md)
