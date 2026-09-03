# UpdateVP

## Description
Updates the specified viewport: a dirty viewport, whose render type is other than wireframe, will be re-rendered.

```pascal
PROCEDURE UpdateVP(viewportHandle : HANDLE);
```

```python
def vs.UpdateVP(viewportHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|Handle to a viewport|

## Examples
```pascal
SetObjectVariableInt( pioParentVPHand, 1001, pioTuneRenderMode );
{ Set Foreground Render Mode to None }
SetObjectVariableInt( pioParentVPHand, 1036, kRWModeNone );
{ update viewport }
UpdateVP( pioParentVPHand );
{ Return VP to it's original Background RenderMode }
SetObjectVariableInt( pioParentVPHand, 1001, vpBackRenderMode );
{ Return VP to it's original Foreground RenderMode }
SetObjectVariableInt( pioParentVPHand, 1036, vpForeRenderMode );
```
```python
import vs

# Updates the specified viewport: a dirty viewport, whose render type is
# other than wireframe, will be re-rendered.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.UpdateVP(viewportHandle)
```

## Version
Availability: from VectorWorks11.0

## Category
* [Objects - Groups](../Categories/Objects%20-%20Groups.md)
