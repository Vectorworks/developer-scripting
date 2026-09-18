# OLDGetLoadDataReal

## Description
Using selector, gets load data with real value for the parametric object
Available selectors : kDLDSelectorWeight = 5.

```pascal
FUNCTION OLDGetLoadDataReal(
				handle    : HANDLE;
				selector  : INTEGER;
				loadIndex : INTEGER): REAL;
```

```python
def vs.OLDGetLoadDataReal(handle, selector, loadIndex):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|selector|INTEGER|   |
|loadIndex|INTEGER|   |

## Examples
```pascal
realVal	:= OLDGetLoadDataReal( ghParm, kDLDSelectorWeight, 0 );

TTLWeightFromBW	:= OLDGetLoadDataReal( ghParm, kDLDSelectorWeight, 0 );

BEGIN
	realVal	:= OLDGetLoadDataReal( ghParm, kDLDSelectorWeight, 0 );
	IF	Eq( realVal, 0, 1 )
	&	NOT Eq( realVal, oldVal, 1 )		{"&" <> "|"}
	THEN BEGIN
		realVal	:= oldVal * 1000;
```
```python
import vs

# Using selector, gets load data with real value for the parametric object
# Available selectors : kDLDSelectorWeight = 5.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
selector = 1
loadIndex = 1

area = vs.OLDGetLoadDataReal(handle, selector, loadIndex)
vs.Message('OLDGetLoadDataReal returned: ' + str(area))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
