# ConvertToNURBS

## Description
This function converts the input object into a new NURBS object or a group of NURBS objects in the document.

```pascal
FUNCTION ConvertToNURBS(
				h        : HANDLE;
				keepOrig : BOOLEAN): HANDLE;
```

```python
def vs.ConvertToNURBS(h, keepOrig):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle of original object.|
|keepOrig|BOOLEAN|Leave the original object in the drawing.|

## Remarks
[[User:CBM-c-|_c_]] (2010.12.24) The orientation of the generated NURBS object is -like for extrudes- based on the active view. Set the plane of your profile object with [[VS:SetPlanarRefIDToGround]] if you need it planar.

## Examples
[NURBSObject](examples/NURBSObject.md)

## Version
Availability: from VectorWorks 10.0

## Category
* [Objects - NURBS](../Categories/Objects%20-%20NURBS.md)
