# SetPrefLongInt

## Description
Sets the value of the specified VectorWorks preference setting. Used with preference settings requiring a LONGINT value.

A table of preference dialog items and their corresponding IDs may be found in the [Scirpt Appendix](../Appendix/pages/Appendix%20F%20-%20Preference%20Selectors.md).

```pascal
PROCEDURE SetPrefLongInt(
				index : INTEGER;
				value : LONGINT);
```

```python
def vs.SetPrefLongInt(index, value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|Preference item index.|
|value|LONGINT|New value for preference.|

## Remarks
Sets the value of the specified preference to the value passed.   Similar to SetPref() except it works on preferences for long integer values

## Examples
#### VectorScript ####
```pascal
SetPrefLongInt(55,128);
```
#### Python ####
```python

```

```pascal
BEGIN
	SetPrefLongInt( kConstrainMode, kConstrained );
END;

END;	{of CASE theEvent}
SetPrefLongInt (162, gDecimalPrec);

BEGIN
	gDecimalPrec := GetPrefLongInt (162);
	unitsStyle := GetPrefInt (170);
	CASE unitsStyle OF
		1, 3, 4: SetPrefLongInt (162, 3);
		2      : SetPrefLongInt (162, 4);
		5, 10  : SetPrefLongInt (162, 8);
		7      : SetPrefLongInt (162, 2);
		8      : SetPrefLongInt (162, 3);
```
```python
vs.SetPrefLongInt(1, value)
```

## Version
Availability: from VectorWorks9.0

## Category
* [Document Settings](../Categories/Document%20Settings.md)
