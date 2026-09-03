# SetSliderLiveUpdate

## Description
Sets the specified slider to generate events during a drag.

```pascal
PROCEDURE SetSliderLiveUpdate(
				dialogID    : LONGINT;
				componentID : LONGINT;
				liveUpdate  : BOOLEAN);
```

```python
def vs.SetSliderLiveUpdate(dialogID, componentID, liveUpdate):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|liveUpdate|BOOLEAN|   |

## Examples
```pascal
{ Set the slider to live update }
SetSliderLiveUpdate( dialogID, ShuttleSlider_ID, TRUE );
```
```python
import vs

# Sets the specified slider to generate events during a drag.
dialogID = 1
componentID = 2
liveUpdate = True

vs.SetSliderLiveUpdate(dialogID, componentID, liveUpdate)
```

## Version
Availability: from Vectorworks 2010

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
