# SetGradientSliderSelectedMarker

## Description
Sets the selected marker for the specified gradient slider. 

Note: use the number, 1, to specify a color marker and the number, 2, to specify a midpoint marker.

```pascal
PROCEDURE SetGradientSliderSelectedMarker(
				dialogID     : LONGINT;
				componentID  : LONGINT;
				segmentIndex : INTEGER;
				markerType   : INTEGER);
```

```python
def vs.SetGradientSliderSelectedMarker(dialogID, componentID, segmentIndex, markerType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the gradient slider component.|
|componentID|LONGINT|Index to a specific gradient slider component.|
|segmentIndex|INTEGER|Index to segment in which to select marker.|(segment indexes begin with 1)|
|markerType|INTEGER|Type of marker to select.|(1 = color marker, 2 = midpoint marker)|

## Examples
#### VectorScript ####
```pascal
SetGradientSliderSelectedMarker(dialogID, componentID, 4, 2);
{ selects midpoint marker in segment with index of 4 }
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
