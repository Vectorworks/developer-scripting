# GetZoom

## Description
Function GetZoom returns the percentage of the zoom factor in the current document view.

```pascal
FUNCTION GetZoom : REAL;
```

```python
def vs.GetZoom():
    return REAL
```

## Remarks
([[User:CBM-c-|_c_]], 2015.02.27): There are two possibilities to fetch the zoom. Suppose your zoom is 100%:
* GetZoom: returns 100
* GetPrefReal(500): returns 1

[sd 8/18/98]
Returns the percentage of the zoom factor in the current view. (100.0 would be the value if no zooming was done).

## Version
Availability: from VectorWorks 8.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
