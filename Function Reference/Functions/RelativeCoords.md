# RelativeCoords

## Description
Translates a point into a coordinate system defined by 2 other points.

```pascal
FUNCTION RelativeCoords(
				pt    : VECTOR;
				begPt : VECTOR;
				endPt : VECTOR): VECTOR;
```

```python
def vs.RelativeCoords(pt, begPt, endPt):
    return VECTOR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt|VECTOR|   |
|begPt|VECTOR|   |
|endPt|VECTOR|   |

## Remarks
([[User:CBM-c-|_c_]], 2022.01.19) In Python the tuple returned is always bidimensional in the form (0.0, 0.0).
Remember to add a third item (0.0, 0.0, 0.0) for usage in the vector Routines such as VS:Vec2Ang or they will return gibberish.

See graphical representation below (click on the image to enlarge it):

[[File:C_MathRelativeCoords.png|200px ]] 

[MaKro 11/2021] Did not dig deeper, but looks like beg and end can be interpreted as: vs.RelativeCoords(p, p_origin, x_axis)

## Examples
#### VectorScript ####
```python
PROCEDURE Example;
VAR
    pt, beg_pt, end_pt, v :VECTOR;

BEGIN
    Message('Set begin point');
    CallTool(-221); { creates a locus }
    GetLocPt(FSActLayer, beg_pt.x, beg_pt.y);

    Message('Set end point');
    CallTool(-221); { creates a locus }
    GetLocPt(FSActLayer, end_pt.x, end_pt.y);

    Message('Set point');
    CallTool(-221); { creates a locus }
    GetLocPt(FSActLayer, pt.x, pt.y);

    v := RelativeCoords(pt, beg_pt, end_pt);
    Message('result vector=', v);
    Locus(v.x, v.y);
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
