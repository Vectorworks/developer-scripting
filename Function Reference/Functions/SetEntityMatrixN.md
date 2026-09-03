# SetEntityMatrixN

## Description
Sets the matrix of the plane for a planar object. If there is already a plane in the document with that matrix, the object will be set to be in that plane. Otherwise a new plane will be added to the document.

```pascal
FUNCTION SetEntityMatrixN(
				objectHandle : HANDLE;
				u            : REAL;
				v            : REAL;
				w            : REAL;
				offset       : REAL): BOOLEAN;
```

```python
def vs.SetEntityMatrixN(objectHandle, u, v, w, offset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|The object whose plane is being set.|
|u|REAL|The X, Y and Z values of the plane's u-vector in current document units.|
|v|REAL|The X, Y and Z values of the plane's v-vector in current document units.|
|w|REAL|The X, Y and Z values of the plane's w-vector in current document units.|
|offset|REAL|The X, Y and Z offsets of the plane in current document units.|

## Examples
```pascal
resultOK := SetEntityMatrixN(objectHandle, 1.0, 2.0, 0.5, 1.5);
```
```python
import vs

# Sets the matrix of the plane for a planar object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
u = 1.0
v = 2.0
w = 2.0
offset = 0.0

ok = vs.SetEntityMatrixN(objectHandle, u, v, w, offset)
if ok:
    vs.Message('SetEntityMatrixN succeeded')
else:
    vs.Message('SetEntityMatrixN failed')
```

## See Also
VS Functions:
[SetEntityMatrix](SetEntityMatrix.md)

## Version
Availability: from Vectorworks 2016

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
