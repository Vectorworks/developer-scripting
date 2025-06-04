# SetSegPt2

## Description
Procedure SetSegPt2 sets the location of the end point of the referenced line or wall object.

```pascal
PROCEDURE SetSegPt2(
				h     : HANDLE;
				pX,pY : REAL);
```

```python
def vs.SetSegPt2(h, p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to arc.|
|p|REAL|New end point of line.|

## Remarks
Although GetSegPt1 works on linear dimensions this call does not successfully set the pt for a dimension.

## See Also
VS Functions:
[SetSegPt1](SetSegPt1.md)

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
