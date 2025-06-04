# GetNumHoles

## Description
Returns the number of openings in the referenced polyline.

```pascal
FUNCTION GetNumHoles(
				inPolyline      : HANDLE;
				VAR outNumHoles : INTEGER): BOOLEAN;
```

```python
def vs.GetNumHoles(inPolyline):
    return (BOOLEAN, outNumHoles)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPolyline|HANDLE|Handle to polyline.|
|outNumHoles|INTEGER|The number of openings in the polyline object.|

## Remarks
This function never returns FALSE regardless of the object type of "inPolyline" or whether "inPolyline" has holes.
It will only return FALSE on "inPolyine" = NIL.

## See Also
VS Functions:
[GetHole](GetHole.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Objects - Polys](../Categories/Objects%20-%20Polys.md)
