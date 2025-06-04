# SetViewMatrix

## Description
Sets view matrix for layer or viewport object.

```pascal
FUNCTION SetViewMatrix(
				objectHandle            : HANDLE;
				offsetX,offsetY,offsetZ : REAL;
				rotationXAng            : REAL;
				rotationYAng            : REAL;
				rotationZAng            : REAL): BOOLEAN;
```

```python
def vs.SetViewMatrix(objectHandle, offset, rotationXAng, rotationYAng, rotationZAng):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|   |
|offset|REAL|   |
|rotationXAng|REAL|   |
|rotationYAng|REAL|   |
|rotationZAng|REAL|   |

## Version
Availability: from VectorWorks10.5

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
