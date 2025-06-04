# ClearGradientSliderSegments

## Description
Removes all segments (except for 2) from the gradient slider.

Note: a gradient slider must always have at least 2 segments.

```pascal
PROCEDURE ClearGradientSliderSegments(
				dialogID    : LONGINT;
				componentID : LONGINT);
```

```python
def vs.ClearGradientSliderSegments(dialogID, componentID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|Index to the dialog layout that contains the gradient slider component.|
|componentID|LONGINT|Index to a specific gradient slider component.|

## Examples
#### VectorScript ####
```pascal
ClearGradientSliderSegments(dialogID, componentID);
```
#### Python ####
```python
vsClearGradientSliderSegments(dialogID, componentID)
```

## Version
Availability: from VectorWorks10.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
