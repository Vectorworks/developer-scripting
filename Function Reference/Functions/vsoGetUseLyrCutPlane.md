# vsoGetUseLyrCutPlane

## Description
Indicates whether an object is observing the layer cut plane

```pascal
PROCEDURE vsoGetUseLyrCutPlane(usingLyrCutPLane : BOOLEAN);
```

```python
def vs.vsoGetUseLyrCutPlane(usingLyrCutPLane):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|usingLyrCutPLane|BOOLEAN|   |

## Examples
```pascal
vsoGetUseLyrCutPlane(TRUE);
```
```python
import vs

# Indicates whether an object is observing the layer cut plane.
usingLyrCutPLane = True

vs.vsoGetUseLyrCutPlane(usingLyrCutPLane)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Events](../Categories/Object%20Events.md)
