# HO_GetHoistColorLbl

## Description
Get the color index of the hoist lable for truss analysis.

```pascal
FUNCTION HO_GetHoistColorLbl(
				value          : REAL;
				maxValue       : REAL;
				VAR colorIndex : INTEGER): BOOLEAN;
```

```python
def vs.HO_GetHoistColorLbl(value, maxValue):
    return (BOOLEAN, colorIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|value|REAL|   |
|maxValue|REAL|   |
|colorIndex|INTEGER|   |

## Examples
```pascal
BEGIN
	value := Str2Num( GetRField( HoistHdl, PIOName, 'ReactionForce' ) );
	maxValue := Str2Num( GetRField( HoistHdl, PIOName, 'MaximumLoad' ) ) * 0.00981;
	useBrxColor := HO_GetHoistColorLbl( value, maxValue, BrxColorIndex );
END;
```
```python
import vs

# Get the color index of the hoist lable for truss analysis.
value = 1.0
maxValue = 2.0

ok, colorIndex = vs.HO_GetHoistColorLbl(value, maxValue)
vs.Message('HO_GetHoistColorLbl returned: ' + str((ok, colorIndex)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Spotlight](../Categories/Spotlight.md)
