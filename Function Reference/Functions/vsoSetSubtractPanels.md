# vsoSetSubtractPanels

## Description
Used during event 58 to retrun whether a curtain wall object will have the wall subtract the panel from the frames

```pascal
PROCEDURE vsoSetSubtractPanels(inSubtractPanels : BOOLEAN);
```

```python
def vs.vsoSetSubtractPanels(inSubtractPanels):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inSubtractPanels|BOOLEAN|   |

## Examples
```pascal
vsoSetSubtractPanels(TRUE);
```
```python
import vs

# Used during event 58 to retrun whether a curtain wall object will have the
# wall subtract the panel from the frames.
inSubtractPanels = True

vs.vsoSetSubtractPanels(inSubtractPanels)
```

## Version
Availability: from Vectorworks 2015

## Category
* [Object Events](../Categories/Object%20Events.md)
