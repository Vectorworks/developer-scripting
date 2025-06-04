# Split2DObjectByLine

## Description
Splits objectHd along a line defined by the two points.

```pascal
PROCEDURE Split2DObjectByLine(
				objectHd    : HANDLE;
				p1X,p1Y     : REAL;
				p2X,p2Y     : REAL;
				VAR listHds : HANDLE);
```

```python
def vs.Split2DObjectByLine(objectHd, p1, p2):
    return listHds
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|   |
|p1|REAL|   |
|p2|REAL|   |
|listHds|HANDLE|   |

## Remarks
Charles Chandler [2007.03.10]: This call needs some more work. It sometimes fails, and when it succeeds, it only returns one poly. It should return a group containing both pieces of the result of splitting the object.

[[User:Orso.B.Schmid|orso]] [2010.09.04]: "listHds" is a placeholder which you'll use to navigate the objects created by this routine. They won't draw immediately, you need to "materialize" them using [[VS:CreateDuplicateObject| CreateDuplicateObject]] or [[VS:ConvertToPolygon| ConvertToPolygon]]. The number of objects created can be none (NIL) or more, according to the geometry of your source object "objectHd" and the splitting coordinates p1, p2.

[[User:Orso.B.Schmid|orso]] [2008.04.26]: The handle "listHds", if not NIL, is always the right portion of the clipped object. You can access the left portion through [[VS:NextObj| NextObj]](listHds).

[[User:Orso.B.Schmid|orso]] [2010.09.04]: WARNING: This routine can cause crash if used in plug-in objects. Upon copying and pasting in a new document a PIO instance that uses this routine, the application will crash. (Tested VW13-15).

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
polyHandle :HANDLE;
lineHandle :HANDLE;
resultHandle :HANDLE;
begPt :VECTOR;
endPt :VECTOR;
BEGIN
CallTool(-204); polyHandle := FSActLayer;
CallTool(-201); lineHandle := FSActLayer;
GetSegPt1(lineHandle, begPt.x, begPt.y);
GetSegPt2(lineHandle, endPt.x, endPt.y);
Split2DObjectByLine(polyHandle, begPt.x, begPt.y, endPt.x, endPt.y, resultHandle);
resultHandle := CreateDuplicateObject(resultHandle, NIL);
END;
RUN(Example);
```

```pascal
{ .... }
{ use the placeholder "listHds" to generate on drawing the objects resulting from Split2DObjectByLine, if any }
Split2DObjectByLine(polyHandle, p1x, p1y, p2x, p2y, listHds);
IF listHds <> NIL THEN BEGIN
	right_h := CreateDuplicateObject(listHds, NIL); { right part of the clipped poly }

	IF NextObj(listHds) <> NIL THEN
		left_h := CreateDuplicateObject(NextObj(listHds), NIL); { left part of the clipped poly, but you could have more }

END;
{ .... }
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks 12.0

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
