# GetUnits

## Description
Procedure GetUnits returns the current units settings of the document.

{| class="wikitable_c"
|+ Table - Units Formats
! Units Format
! Constant
|-
| Decimal
| style="text-align:center"| 0
|-
| Fractional
| style="text-align:center"| 1
|-
| Decimal Ft/Inches
| style="text-align:center"| 2
|-
| Fractional Ft/Inches
| style="text-align:center"| 3
|}

More extensive Units information is available using the [[VS:GetPref]] routines with the selectors shown in the tables of the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md#primary-units-selectors).

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

## Version
Availability: from All Versions

## Category
* [Units](../Categories/Units.md)
