# SetProjectElevation

## Description
Set project elevation.

```pascal
PROCEDURE SetProjectElevation(projElev : REAL);
```

```python

def vs.SetProjectElevation(projElev):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|projElev|REAL||

## Examples
```pascal
1: BEGIN {OK button}
	ValidateProjElev;
	{ projectElev must always be in millimeters before save it }
	SetProjectElevation(projectElev);
	IF (gFirstTimeSheets) AND (gIsFirstTimeModel) THEN gSetupRecord.FloorPlanScale := layerScale;
	gSetupRecord.Units := dwgUnits;
	GetBooleanItem( dlogID, kTitleBlockBorderGroupBox	, gUseTBB		 );
	GetBooleanItem( dlogID, kTitleBlockSecCheckBox		, gDrawBorderNow );
```
```python
import vs

# Set project elevation.
projElev = 0.0

vs.SetProjectElevation(projElev)
```

## Version
Availability: from Vectorworks 2024

## Category
* [GIS](../Categories/GIS.md)
