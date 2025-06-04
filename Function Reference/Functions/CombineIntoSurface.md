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

## Version
Availability: from VectorWorks 10.1

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
