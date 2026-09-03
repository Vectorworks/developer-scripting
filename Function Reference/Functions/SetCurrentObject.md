# SetCurrentObject

## Description
Procedure SetCurrentObject sets the referenced object to be the current object of the document. The current object is defined as the last object created, and can be referenced by LNewObj.

```pascal
PROCEDURE SetCurrentObject(h : HANDLE);
```

```python
def vs.SetCurrentObject(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
```pascal
h1 := LNewObj;
Arc (-r2, r2, r2, -r2, 0, 360);
h2 := LNewObj;
ClipSurface (h1, h2);
SetCurrentObject (PrevObj (h2));
DelObject (h2);
```
```python
import vs

# Procedure SetCurrentObject sets the referenced object to be the current
# object of the document.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.SetCurrentObject(h)
```

## Version
Availability: from MiniCAD4.0

## Category
* [Utility](../Categories/Utility.md)
