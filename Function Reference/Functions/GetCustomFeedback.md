# GetCustomFeedback

## Description
Gets the group of objects attached to a parametric used only for display on screen, this group will not export or print.

```pascal
FUNCTION GetCustomFeedback(
				ParametricHandle  : HANDLE;
				VAR FeedbackGroup : HANDLE): Boolean;
```

```python
def vs.GetCustomFeedback(ParametricHandle):
    return (Boolean, FeedbackGroup)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ParametricHandle|HANDLE|The parametric object to which the feedback group was added.|
|FeedbackGroup|HANDLE|The feedback group that was attached to the Parametric Object.|

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
