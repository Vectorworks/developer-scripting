# ConvertToArcPolyline

## Description
Convert, within a tolerance, the input polyline into an polyline that uses arcs for the curves.

```pascal
FUNCTION ConvertToArcPolyline(
				hPolygon : HANDLE;
				dFuzz    : REAL): HANDLE;
```

```python
def vs.ConvertToArcPolyline(hPolygon, dFuzz):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hPolygon|HANDLE|   |
|dFuzz|REAL|   |

## Remarks
(*\_c\_*, 2022.02.02) This routine must be updated, it still doesn't recognize Radius vertexes. 

As of VW 2022  the routine behaves on vertexes as such:
* corner: preserved
* arc: preserved only on dFuzz = 0, otherwise they turn into corner, which is truly strange, since the purpose IS to create arc vertexes
* radius: ignored, turn into corner
* cubic: turn into arc
* bezier: turn into arc

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
    polyObj, newPolyObj : HANDLE;
	
BEGIN
    { select a polyline }
    polyObj := FSActLayer;
    IF polyObj <> NIL THEN BEGIN
        newPolyObj := ConvertToArcPolyline(polyObj, 0);
        SetDSelect(polyObj);
    END;
END;
Run(Test);
```
#### Python ####
```python
# select a polyline
polyObj = vs.FSActLayer()
if polyObj != vs.Handle( 0 ):
	newPolyObj = vs.ConvertToArcPolyline(polyObj, 0)
	vs.SetDSelect(polyObj)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
