# IsObjectFlipped

## Description
Function IsObjectFlipped returns the flip orientation of the specified 3D object. The function returns TRUE if the object is currently flipped.  

This function works for sweeps, extrudes, multiple extrudes, symbols, solids, layer references, and plug-in objects.

```pascal
FUNCTION IsObjectFlipped(h : HANDLE): BOOLEAN;
```

```python
def vs.IsObjectFlipped(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Returns true if the object is currently flipped.  Works for sweeps, extrudes, mextrudes, symbols, solids, layer refs, and plug-in objects

[sd 8/19/98]

## Examples
==== VectorScript ====
```pascal
FUNCTION ObjFlippedInWall(objH, wallH :HANDLE) :BOOLEAN;
BEGIN
ObjFlippedInWall := ((Trunc(GetSymRot(objH)) &lt;&gt; Trunc(HAngle(wallH))) = IsObjectFlipped(objH)); 
END;
```
==== Python ====
```python

```

## See Also
VS Functions:
[IsFlipped](IsFlipped.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
