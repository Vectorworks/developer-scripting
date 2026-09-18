# ValidAngStr

## Description
Function ValidAngStr returns TRUE if the specified value can be converted into a numeric angle value. If TRUE, the value (in decimal degrees) of the string is returned.

```pascal
FUNCTION ValidAngStr(
				str       : STRING;
				VAR value : REAL): BOOLEAN;
```

```python
def vs.ValidAngStr(str):
    return (BOOLEAN, value)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|str|STRING|String value to be checked for angle validity.|
|value|REAL|Returns numeric angle value converted from input string.|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
str :STRING;
value :REAL;
BEGIN
str := StrDialog('Enter the angle:', 'N10E');
IF ValidAngStr(str, value) THEN Message(value);
END;
RUN(Example);
```
#### Python ####
```python

```

```pascal
	ok := TRUE;
	outBearing := Compass2Cad(outBearing);
END;
{Azimuth or Bearing, Decimal or DMS}
IF NOT ok THEN if ValidAngStr(inBearingStr, outBearing) then BEGIN
	ok := TRUE;
	{Azimuth-DMS}
	IF ValidNumStr(Copy(inBearingStr, 1, 1), num) THEN outBearing := Compass2Cad(outBearing);
END;

BEGIN
{** Get all needed dialog data here.}
	GetItemText(dlogID, 14, tmpStr);
	noError := ValidAngStr(tmpStr, gLatitude);

	tmpStr := Num2Str(8, tmpReal);
	if Pos('.', tmpStr) > 0 then while Copy(tmpStr, Len(tmpStr), 1) = '0' DO tmpStr := Copy(tmpStr, 1, Len(tmpStr) - 1);
	IF Copy(tmpStr, Len(tmpStr), 1) = '.' THEN tmpStr := Copy(tmpStr, 1, Len(tmpStr) - 1);
END else if Pos(fldType, 'r10') > 0 then BEGIN {If it's an angle field, convert it to a real.}
	tmpBoo := ValidAngStr(valueVa, tmpReal);
	tmpStr := Num2Str(8, tmpReal);
	while Copy(tmpStr, Len(tmpStr), 1) = '0' DO tmpStr := Copy(tmpStr, 1, Len(tmpStr) - 1);
END;
```
```python
result = vs.ValidAngStr('Example')
```

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
