# vsoWidgetPopupGetCnt

## Description
?

```pascal
FUNCTION vsoWidgetPopupGetCnt(widgetID : LONGINT): LONGINT;
```

```python
def vs.vsoWidgetPopupGetCnt(widgetID):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |

## Examples
```pascal
BEGIN
	IF (vsoWidgetPopupGetCnt(kShapeChoice) = 0) |  (GetRfield(ParamHandle,ParamName,'Shape')='') THEN
	BEGIN
		PopulateList;
	END;
```
```python
import vs

# ?.
widgetID = 1

resultN = vs.vsoWidgetPopupGetCnt(widgetID)
vs.Message('vsoWidgetPopupGetCnt returned: ' + str(resultN))
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Object Events](../Categories/Object%20Events.md)
