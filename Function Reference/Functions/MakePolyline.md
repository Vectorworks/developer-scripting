# MakePolyline

## Description
Creates a polyline using inSourceObject. inSourceObject is unchanged.

```pascal
FUNCTION MakePolyline(inSourceObject : HANDLE): HANDLE;
```

```python
def vs.MakePolyline(inSourceObject):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inSourceObject|HANDLE|The 2D object from which to make a polyline.|

## Remarks
Creates a polyline from inSourceObject. inSourceObject is unchanged.


This routine does not delete inSourceObject; also it creates its returned object not as the last object in the active layer, but immediately after inSourceObject in the stacking order, so if you delete inSourceObject, you will have "replaced" it.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h,h2:HANDLE;
BEGIN
h:=FSActLayer;
h2 := MakePolyline(h);
DelObject(h);
END;
RUN(Example);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks10.1

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
