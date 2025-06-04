# SetBBox

## Description
Procedure SetBBox positions objects whose geometry is defined by a bounding box. These objects currently are Image, PICT, Rectangle, Oval, Rounded Rectangle, and Worksheet Container. 

Other objects will generate a warning if they are passed to SetBBox.

```pascal
PROCEDURE SetBBox(
				h       : HANDLE;
				p1X,p1Y : REAL;
				p2X,p2Y : REAL);
```

```python
def vs.SetBBox(h, p1, p2):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|p1|REAL|Top left coordinate of bounding box.|
|p2|REAL|Bottom right coordinate of bounding box.|

## Remarks
This function should be obsleted and replaced by a function which can only move objects and not corrupt other bounding boxes. [PCP]
For objects which are defined by their box, such as rectangles &amp; ovals, this function allows that box to be changed.  [sd 8/14/98]

[Joel Sciamma 2007.05.11]: Use it to resize the supported objects by moving the vertices of the bounding box as you might change the dimensions of a selected object in the Object Info palette. If you specify values that would cause the top left vertex to be below or to the right of the bottom right vertex, the referenced object will be moved, not resized. Call ResetObject after this procedure to force the object to redraw

## Examples
==== VectorScript ====
```pascal
{ To reshape a rect whose top left coordinates are 23.5, 100 and bottom right are 92, 49: }
SetBBox(ObjHandle, 28, 110, 80.5, 49);
ResetObject(ObjHandle);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
