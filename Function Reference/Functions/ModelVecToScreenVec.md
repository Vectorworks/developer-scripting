# ModelVecToScreenVec

## Description
Takes Data from one space to another.

```pascal
PROCEDURE ModelVecToScreenVec(VAR pX,pY : REAL);
```

```python
def vs.ModelVecToScreenVec(p):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|   |

## Remarks
This routine transforms a given vector from model(object) to VCS.

## Examples
```pascal
IF GetObjectVariableBoolean(theOtherOne,650) THEN BEGIN
	Move3DObj(theOtherOne, thatPt.x, thatPt.y, 0);
END ELSE BEGIN
	{ thatPt is a vector in model space,but HMove translates objects in screen space,I think. }
	ModelVecToScreenVec( thatPt.x,thatPt.y );
	HMove(theOtherOne, thatPt.x, thatPt.y);
END;
```
```python
import vs

# Takes Data from one space to another.
p = (0, 0)

result = vs.ModelVecToScreenVec(p)
```

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
