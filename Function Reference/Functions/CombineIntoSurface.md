# CombineIntoSurface

## Description
Creates a polyline from the bounded selection surrounding the given point.

```pascal
FUNCTION CombineIntoSurface(ptX, ptY : REAL): HANDLE;
```

```python
def vs.CombineIntoSurface(pt):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pt|REAL|A point within the bounded selection.|

## Remarks
[[User:Orso.b.schmid|Orso]] (2011 Jan. 30): The routine stopped working for boundaries made of walls in VW 2011 (tested SP2).

## Examples
```pascal
resultH := CombineIntoSurface(1.0, 2.0);
```
```python
import vs

# Creates a polyline from the bounded selection surrounding the given point.
pt = (0, 0)

objHandle = vs.CombineIntoSurface(pt)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks 10.1

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
