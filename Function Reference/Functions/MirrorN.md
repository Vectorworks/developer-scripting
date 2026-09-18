# MirrorN

## Description
Reflect an object across an axis.<BR>
<BR>
For a 2D reflection, the axis is a line containing arbitrary point p and extending along vector v.<BR>
<BR>
The difference with Mirror, when preserveMatrix is set to true, is that this function preserves the matrix of the objects that have one, which leads to better visual results.

```pascal
FUNCTION MirrorN(
				h              : HANDLE;
				dup            : BOOLEAN;
				p1             : REAL;
				p2             : REAL;
				preserveMatrix : BOOLEAN): HANDLE;
```

```python
def vs.MirrorN(h, dup, p1, p2, preserveMatrix):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The object to reflect|
|dup|BOOLEAN|If false, transform the original object to the new position. If true, create a new object|
|p1|REAL|An arbitrary point on the mirror axis|
|p2|REAL|A second arbitrary point on the mirror axis|
|preserveMatrix|BOOLEAN|When this parameter is set to false, then this function works exactly the same as Mirror. Otherwise, objects that have matrices, such as Symbols and PIOs, get their matrices updated correctly with the mirror matrix, leading to better visual results.|

## Examples
```pascal
resultH := MirrorN(h, TRUE, 1.0, 2.0, FALSE);
```
```python
import vs

# Reflect an object across an axis.
h = vs.FSActLayer()  # handle to the first selected object on the active layer
dup = True
p1 = 1.0
p2 = 2.0
preserveMatrix = True

objHandle = vs.MirrorN(h, dup, p1, p2, preserveMatrix)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2023

## Category
* [Object Editing](../Categories/Object%20Editing.md)
