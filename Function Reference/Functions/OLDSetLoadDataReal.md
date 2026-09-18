# OLDSetLoadDataReal

## Description
Using selector, sets load data with real value for the parametric object.
Available selectors : kDLDSelectorWeight = 5.

```pascal
PROCEDURE OLDSetLoadDataReal(
				handle    : HANDLE;
				selector  : INTEGER;
				value     : REAL;
				loadIndex : INTEGER);
```

```python
def vs.OLDSetLoadDataReal(handle, selector, value, loadIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|selector|INTEGER|   |
|value|REAL|   |
|loadIndex|INTEGER|   |

## Examples
```pascal
BEGIN
	realVal	:= oldVal * 1000;
	OLDSetLoadDataReal( ghParm, kDLDSelectorWeight, realVal, 0 );
END;

BEGIN
	NewBxWeight	:= BxWeightFromOIP * 1000;
	OLDSetLoadDataReal( ghParm, kDLDSelectorWeight, NewBxWeight+YokeWeightFromOIP, 0 );
	SetRField (ghParm, kPIOName, 'BxWeight',Concat(OLDMassRealToStr(NewBxWeight)));
END;

IF	Eq( realVal, 0, 1 )
&	NOT Eq( realVal, oldVal, 1 )		{"&" <> "|"}
THEN BEGIN
	realVal	:= oldVal * 1000;
	OLDSetLoadDataReal( ghParm, kDLDSelectorWeight, realVal, 0 );
	SetRField (ghParm, kPIOName, 'BumpWeight',Concat(OLDMassRealToStr(realVal)));
END;
```
```python
import vs

# Using selector, sets load data with real value for the parametric object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
selector = 1
value = 1.0
loadIndex = 1

vs.OLDSetLoadDataReal(handle, selector, value, loadIndex)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
