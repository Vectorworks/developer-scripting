# HasConstraint

## Description
Returns whether the referenced object has a parametric constraint .

```pascal
FUNCTION HasConstraint(h : HANDLE): BOOLEAN;
```

```python
def vs.HasConstraint(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
([[User:CBM-c-|_c_]], 2011 Oct. 06): This call returns true when there is an object of type 110 attached. This could mean an associated dimension, a join (for walls) or any user defined constraint. ONE constraint can be fetched using GetObjectVariableHandle(h, 703), but that brings nowhere, since there seems to be no way to fetch the related (constrained) object(s). Nevertheless fetching the first object of type 110 allows to parse for others using NextObj(my110obj) and checking for object type.
Any vertex constrained creates one such object type 110 for each of the objects involved.

## Version
Availability: from VectorWorks 9.0

## Category
* [Parametric Constraints](../Categories/Parametric%20Constraints.md)
