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

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
