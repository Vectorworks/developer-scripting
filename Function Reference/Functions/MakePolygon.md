# MakePolygon

## Description
MakePolygon creates a 2D Polygon using inSourceObject. Does not delete inSourceObject.

```pascal
FUNCTION MakePolygon(inSourceObject : HANDLE): HANDLE;
```

```python
def vs.MakePolygon(inSourceObject):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inSourceObject|HANDLE|inSource object should be a 2D object that can be polygonalized.|

## Remarks
This routine creates its returned object not as the last object in the active layer, but immediately after inSourceObject in the stacking order, so if you delete inSourceObject, you will have "replaced" it.


See also: &lt;a href=http://www.vectorworks.net/support/custom/vscript/reference/asp/main.asp?name=ConvertToPolygon&gt;ConvertToPolygon&lt;/a&gt;.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
h :HANDLE;
BEGIN
CallTool(-204);
h := FSActLayer;
h := MakePolygon(h);
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
