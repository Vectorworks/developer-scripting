# GetGradientSliderSelectedMarker

## Description
Gets the selected marker for the specified gradient slider. 

Note: use the number, 1, to identify a color marker and the number, 2, to identify a midpoint marker.

```pascal
PROCEDURE GetGradientSliderSelectedMarker(
				dialogID         : LONGINT;
				componentID      : LONGINT;
				VAR segmentIndex : INTEGER;
				VAR markerType   : INTEGER);
```

```python
def vs.GetGradientSliderSelectedMarker(dialogID, componentID):
    return (segmentIndex, markerType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the gradient slider component.|
|componentID|LONGINT|Index to a specific gradient slider component.|
|segmentIndex|INTEGER|Index to segment containing selected marker.|(segment indexes begin with 1)|
|markerType|INTEGER|Type of marker selected.|(1 = color marker, 2 = midpoint marker)|

## Examples
==== VectorScript ====
```pascal
GetGradientSliderSelectedMarker(dialogID, componentID, segmentIndex, markerType);
```
==== Python ====
```python
segmentIndex, markerType = vs.GetGradientSliderSelectedMarker(dialogID, componentID)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
