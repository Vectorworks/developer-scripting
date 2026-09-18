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

## Examples
```pascal
resultOK := GetCustomFeedback(ParametricHandle, FeedbackGroup);
```
```python
import vs

# Gets the group of objects attached to a parametric used only for display on
# screen, this group will not export or print.
ParametricHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, FeedbackGroup = vs.GetCustomFeedback(ParametricHandle)
vs.Message('GetCustomFeedback returned: ' + str((ok, FeedbackGroup)))
```

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
