# ScreenVecToModelVec

## Description
Takes data from one space to another

```pascal
PROCEDURE ScreenVecToModelVec(VAR pX,pY : REAL);
```

```python
def vs.ScreenVecToModelVec(p):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|   |

## Remarks
This routine transform  a given point from VCS(object) to Model.  Ignores the translation of the plan rotation matrix. Just takes into account the rotation

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
