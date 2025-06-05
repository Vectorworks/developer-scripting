# GetVCenter

## Description
Procedure GetVCenter returns the VectorWorks document coordinates at the center of the drawing window.

```pascal
PROCEDURE GetVCenter(VAR centerX,centerY : REAL);
```

```python
def vs.GetVCenter():
    return center
```

## Parameters
|Name|Type|Description|
|---|---|---|
|center|REAL|Returns view center point.|

## Remarks
([[User:CBM-c-|_c_]], 2015.03.01):  This is not to be confused with the center of the page. The view center is always the center of the open window, so if you resize the window or pan somewhere else, for example, the view center will move accordingly.

## Examples

## Version
Availability: from VectorWorks 8.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
