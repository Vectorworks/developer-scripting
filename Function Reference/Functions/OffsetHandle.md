# OffsetHandle

## Description
Creates a group of lines which represent the weighted medial axis of given polygon.

```pascal
FUNCTION OffsetHandle(
				h                : HANDLE;
				offsetDistance   : REAL;
				EdgeRestoration  : BOOLEAN;
				FilletSharpEdges : BOOLEAN): HANDLE;
```

```python
def vs.OffsetHandle(h, offsetDistance, EdgeRestoration, FilletSharpEdges):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|offsetDistance|REAL|   |
|EdgeRestoration|BOOLEAN|   |
|FilletSharpEdges|BOOLEAN|   |

## Remarks
([[User:CBM-c-|_c_]], 2014.03.25): The routine was introduced undocumented by VW11 (2006). 
Warning: 
* The parameter ''offsetDistance'' takes mm, unregarded unit's settings. 
* If you pass a polygon/polyline it outputs a group containing one or more polygon/polylines, not a group of lines.
* Polyline holes are ignored
* Undo fails on this action: you should consider carefully if using this routine

; VW 2011, 2012, 2013: the handle ''h'' doesn't set. Use [[VS:LObject| LObject]] to fetch the handle. This is dangerous, if the routine fails, LObject will be something else: store LObject before running the script and afterwards, then compare. If they are different the routine succeeded.
; VW 2014: the handle will set as expected, undo still fails

## Examples
#### VectorScript ####
```pascal
PROCEDURE try;
VAR
	prevLObj, sourceObj, groupObj : HANDLE;
BEGIN
	sourceObj := FSActLayer;
	IF (sourceObj <> NIL) THEN BEGIN

		{ h won't set with OffsetHandle until VW 2014 }
		prevLObj := LObject; { only before VW 2014: store for later comparison }

		groupObj := OffsetHandle(sourceObj, -10, TRUE, TRUE); { negative offset -10mm }
		groupObj := LObject; { only before VW 2014: this should be now the product of OffsetHandle }

		IF (prevLObj <> groupObj) THEN BEGIN
			Message('Type: ', GetType(groupObj));
			ResetObject(groupObj);
			HUngroup(groupObj);
			SetDSelect(sourceObj);
		END;
	END;
END;
Run(try);
```
#### Python ####
```python

```

## See Also
Similar calls:
* [OffsetPoly](OffsetPoly.md)
* [OffsetPolyN](OffsetPolyN.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Object Editing](../Categories/Object%20Editing.md)
