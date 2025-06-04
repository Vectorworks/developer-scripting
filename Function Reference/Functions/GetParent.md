# GetParent

## Description
Returns a handle to the parent container object of the referenced object. If the object does not have a container, a handle to the objects' layer will be returned.

```pascal
FUNCTION GetParent(h : HANDLE): HANDLE;
```

```python
def vs.GetParent(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
This is from the SDK documentation for ParentObject():

Returns the "parent" of h, that is, h's immediate owner.  For most objects, this is the layer they are in; for an object in a container, it is its enclosing container; for a layer, it is the drawing header.  The drawing header and any symbol definitions which are not in any folder have no parent; calling ParentObject on them will return nil.

## Version
Availability: from VectorWorks8.5

## Category
* [Object Info](../Categories/Object%20Info.md)
