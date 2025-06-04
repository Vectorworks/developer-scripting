# CreateOffsetNurbsObjectHandle

## Description
Returns a handle to a NURBS object that is offset from the given NURBS object h by the offset distance.

```pascal
FUNCTION CreateOffsetNurbsObjectHandle(
				h              : HANDLE;
				offsetDistance : REAL): HANDLE;
```

```python
def vs.CreateOffsetNurbsObjectHandle(h, offsetDistance):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|offsetDistance|REAL|Offset distance. Positive offsets outwards.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
h :handle;
BEGIN
CallTool(-204);
h := FSActLayer;
h := ConvertToNURBS(h, false);
h := CreateOffsetNurbsObjectHandle(h, 1);
END;
RUN(Example);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
