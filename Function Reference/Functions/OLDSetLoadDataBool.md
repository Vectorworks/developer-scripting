# OLDSetLoadDataBool

## Description
Using selector, sets load data with bool value for the parametric object

```pascal
PROCEDURE OLDSetLoadDataBool(
				handle    : HANDLE;
				selector  : INTEGER;
				value     : BOOLEAN;
				loadIndex : INTEGER);
```

```python
def vs.OLDSetLoadDataBool(handle, selector, value, loadIndex):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|handle|HANDLE|   |
|selector|INTEGER|   |
|value|BOOLEAN|   |
|loadIndex|INTEGER|   |

## Examples
```pascal
OLDSetLoadDataBool(gHParm,kDLDEnableWeightWidget,FALSE,0);	{Object Load Data Weight Widget Disabled}

BEGIN
	OLDSetLoadDataBool(ghParm, kDLDSelectorAttachingEnabled, TRUE, kLoadProjector2Index);
	IF (GetRField(ghParm, kPIOName,'ProjLayout') = 'Stacked')
			THEN
		SetProjectorHang( Proj1Hnd , kLoadProjector2Index) {Load Point aligned w. that of top projector}
				ELSE
```
```python
import vs

# Using selector, sets load data with bool value for the parametric object.
handle = vs.FSActLayer()  # handle to the first selected object on the active layer
selector = 1
value = True
loadIndex = 1

vs.OLDSetLoadDataBool(handle, selector, value, loadIndex)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Truss Analysis](../Categories/Truss%20Analysis.md)
