# GetLayer

## Description
Function GetLayer returns a handle to the layer of the referenced object.

```pascal
FUNCTION GetLayer(h : HANDLE): HANDLE;
```

```python
def vs.GetLayer(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Care should be taken when using this call in the code for an object. If an object is cut-n-pasted or inserted from the object browser, it has to regenerate before it is actually in a layer, in which case GetLayer(h) will return a nil handle. So always check that you have a valid handle before proceeding. (This may have been fixed -- ask Jeff Koppi about this.)

## Examples
#### VectorScript ####
```pascal
LayerHandle:=GetLayer(ObjHd);
```
#### Python ####
```python
LayerHandle = vs.GetLayer(ObjHd)
```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
