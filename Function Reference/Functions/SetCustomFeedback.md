# SetCustomFeedback

## Description
Attaches a group of objects to a parametric used only for display on screen, this group will not export or print.

```pascal
FUNCTION SetCustomFeedback(
				ParametricHandle : HANDLE;
				FeedbackGroup    : HANDLE): Boolean;
```

```python
def vs.SetCustomFeedback(ParametricHandle, FeedbackGroup):
    return Boolean
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ParametricHandle|HANDLE|The parametric object to which the feedback group will be added.|
|FeedbackGroup|HANDLE|The feedback group which will only display on screen.|

## Examples
```pascal
BEGIN
LinkSymbol := MakeLinkSymbol(p1x ,p1y, 90,.375*MarkerScale);
HRotate(LinkSymbol,(p2x+p1x)/2,(p2y+p1y)/2,-GetSymRot(pluginH));
CreatedFeedbackGroup := SetCustomFeedback(pluginH, LinkSymbol);
END;

BEGIN
LinkSymbol := MakeLinkSymbol(p1x ,p1y, 90,.75*MarkerScale);
HRotate(LinkSymbol,0,0,-GetSymRot(pluginH));
CreatedFeedbackGroup := SetCustomFeedback(pluginH, LinkSymbol);
END;
```
```python
import vs

# Attaches a group of objects to a parametric used only for display on
# screen, this group will not export or print.
ParametricHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
FeedbackGroup = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

ok = vs.SetCustomFeedback(ParametricHandle, FeedbackGroup)
if ok:
    vs.Message('SetCustomFeedback succeeded')
else:
    vs.Message('SetCustomFeedback failed')
```

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
